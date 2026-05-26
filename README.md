# 📊 API Flow — BookingKhachSan

> **Kiến trúc**: Clean Architecture (4 layers)
> **Pattern**: CQRS + MediatR + Repository

---

## 🏗️ Tổng quan kiến trúc

```mermaid
graph LR
    Client["🌐 Client\n(Postman / Browser)"]
    API["BookingHotel.API\nControllers"]
    APP["BookingHotel.Application\nHandlers / Commands / Queries"]
    INFRA["BookingHotel.Infrastructure\nRepositories / Services"]
    DB[("💾 Database\nSQLite / SQL Server")]
    
    Client -->|"HTTP Request"| API
    API -->|"mediator.Send(command)"| APP
    APP -->|"repository.DoSomething()"| INFRA
    INFRA -->|"EF Core"| DB
    DB -->|"Entity"| INFRA
    INFRA -->|"Entity"| APP
    APP -->|"DTO"| API
    API -->|"JSON Response"| Client
```

---

## 1️⃣ API Quản lý Hotel

### `GET /api/hotels` — Danh sách + Tìm kiếm & Lọc

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant M as IMediator
    participant H as GetHotelsHandler.cs
    participant R as HotelRepository.cs
    participant DB as 💾 Database

    C->>CTL: GET /api/hotels?city=HCM&minStar=3&minPrice=500
    Note over CTL: GetAll([FromQuery] HotelFilterParams filter)
    CTL->>M: mediator.Send(new GetHotelsQuery(filter))
    M->>H: Handle(GetHotelsQuery, CancellationToken)
    H->>R: hotelRepo.GetAllAsync(filter)
    Note over R: - Include Images<br/>- Include Rooms (where !IsDeleted)<br/>- Filter: SearchTerm, City, Country<br/>- Filter: MinStar, MaxStar<br/>- Filter: MinPrice, MaxPrice<br/>- Filter: AmenityIds<br/>- Phân trang: Skip/Take
    R->>DB: SELECT * FROM Hotels WHERE ...
    DB-->>R: List<Hotel>
    R-->>H: PagedResult<Hotel>
    Note over H: items.Select(h => h.ToSummaryDto())<br/>→ chuyển Hotel sang HotelSummaryDto
    H-->>CTL: PagedResult<HotelSummaryDto>
    CTL-->>C: 200 OK { items, totalCount, page, pageSize, totalPages }
```

### `GET /api/hotels/{id}` — Chi tiết Hotel

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant H as GetHotelByIdHandler.cs
    participant R as HotelRepository.cs
    participant DB as 💾 Database

    C->>CTL: GET /api/hotels/{id}
    CTL->>H: mediator.Send(new GetHotelByIdQuery(id))
    H->>R: hotelRepo.GetByIdAsync(id, includeDetails: true)
    Note over R: Include: Images, AmenityMappings+Amenity<br/>Include: Rooms+RoomType
    R->>DB: SELECT với JOIN
    DB-->>R: Hotel entity (đầy đủ)
    R-->>H: Hotel?
    alt Hotel == null
        H-->>CTL: throw NotFoundException("Hotel", id)
        CTL-->>C: 404 Not Found
    else Hotel tồn tại
        H-->>CTL: hotel.ToDto() → HotelDto
        CTL-->>C: 200 OK { id, name, city, images[], amenities[], minRoomPrice }
    end
```

### `POST /api/hotels` — Tạo Hotel

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant H as CreateHotelHandler.cs
    participant R as HotelRepository.cs
    participant DB as 💾 Database

    C->>CTL: POST /api/hotels\n{ name, address, city, starRating... }
    CTL->>H: mediator.Send(CreateHotelCommand)
    Note over H: Tạo new Hotel entity<br/>gán tất cả fields từ command
    H->>R: hotelRepo.CreateAsync(hotel)
    R->>DB: INSERT INTO Hotels
    DB-->>R: Hotel (đã có Id, CreatedAt)
    R-->>H: Hotel entity
    H-->>CTL: created.ToDto() → HotelDto
    CTL-->>C: 201 Created\nLocation: /api/hotels/{newId}\n{ id, name, ... }
```

### `PUT /api/hotels/{id}` — Cập nhật Hotel

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant H as UpdateHotelHandler.cs
    participant R as HotelRepository.cs
    participant DB as 💾 Database

    C->>CTL: PUT /api/hotels/{id}\n{ name, city, starRating... }
    CTL->>H: mediator.Send(new UpdateHotelCommand(id, ...))
    H->>R: hotelRepo.GetByIdAsync(id)
    alt Không tồn tại
        H-->>CTL: throw NotFoundException
        CTL-->>C: 404 Not Found
    else Tồn tại
        Note over H: Cập nhật từng field<br/>Set UpdatedAt = DateTime.UtcNow
        H->>R: hotelRepo.UpdateAsync(hotel)
        R->>DB: UPDATE Hotels SET ...
        DB-->>R: OK
        H-->>CTL: hotel.ToDto()
        CTL-->>C: 200 OK { id, name, ... }
    end
```

### `DELETE /api/hotels/{id}` — Xóa mềm Hotel

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant H as DeleteHotelHandler.cs
    participant R as HotelRepository.cs
    participant DB as 💾 Database

    C->>CTL: DELETE /api/hotels/{id}
    CTL->>H: mediator.Send(new DeleteHotelCommand(id))
    H->>R: hotelRepo.ExistsAsync(id)
    alt Không tồn tại
        H-->>CTL: throw NotFoundException
        CTL-->>C: 404 Not Found
    else Tồn tại
        H->>R: hotelRepo.SoftDeleteAsync(id)
        Note over R: ExecuteUpdateAsync<br/>SET IsDeleted = true<br/>(không xóa vật lý)
        R->>DB: UPDATE Hotels SET IsDeleted=1 WHERE Id=...
        H-->>CTL: void
        CTL-->>C: 204 No Content
    end
```

### `POST/DELETE /api/hotels/{id}/amenities/{amenityId}` — Gắn / Gỡ Tiện ích

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as HotelsController.cs
    participant H as AddHotelAmenityHandler.cs
    participant R as AmenityRepository.cs
    participant DB as 💾 Database

    C->>CTL: POST /api/hotels/{id}/amenities/{amenityId}
    CTL->>H: mediator.Send(new AddHotelAmenityCommand(hotelId, amenityId))
    H->>R: hotelRepo.ExistsAsync(hotelId)
    H->>R: amenityRepo.AddToHotelAsync(hotelId, amenityId)
    Note over R: Kiểm tra đã tồn tại chưa<br/>Nếu chưa: INSERT INTO AmenityMappings
    R->>DB: INSERT INTO AmenityMappings (HotelId, AmenityId)
    CTL-->>C: 204 No Content
```

---

## 2️⃣ API Quản lý Room

### `GET /api/hotels/{hotelId}/rooms` — Danh sách phòng

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as RoomsController.cs
    participant H as GetRoomsByHotelHandler.cs
    participant R as RoomRepository.cs
    participant DB as 💾 Database

    C->>CTL: GET /api/hotels/{hotelId}/rooms
    CTL->>H: mediator.Send(new GetRoomsByHotelQuery(hotelId))
    H->>R: roomRepo.GetByHotelIdAsync(hotelId)
    Note over R: Include RoomType, Include Images<br/>WHERE HotelId = ? AND IsDeleted = false
    R->>DB: SELECT với JOIN
    DB-->>R: List<Room>
    R-->>H: IEnumerable<Room>
    Note over H: rooms.Select(r => r.ToSummaryDto())
    H-->>CTL: IEnumerable<RoomSummaryDto>
    CTL-->>C: 200 OK [ { id, roomNumber, roomTypeName, pricePerNight, isAvailable }... ]
```

### `POST /api/hotels/{hotelId}/rooms` — Tạo phòng mới

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as RoomsController.cs
    participant H as CreateRoomHandler.cs
    participant HR as HotelRepository.cs
    participant RR as RoomRepository.cs
    participant DB as 💾 Database

    C->>CTL: POST /api/hotels/{hotelId}/rooms\n{ roomTypeId, roomNumber, pricePerNight, capacity }
    CTL->>H: mediator.Send(new CreateRoomCommand(hotelId, ...))
    H->>HR: hotelRepo.ExistsAsync(hotelId)
    alt Hotel không tồn tại
        H-->>CTL: throw NotFoundException
        CTL-->>C: 404 Not Found
    else Hotel tồn tại
        Note over H: Tạo new Room entity
        H->>RR: roomRepo.CreateAsync(room)
        RR->>DB: INSERT INTO Rooms
        DB-->>RR: Room (với Id mới)
        H-->>CTL: room.ToDto() → RoomDto
        CTL-->>C: 201 Created { id, roomNumber, pricePerNight, ... }
    end
```

---

## 3️⃣ API Quản lý RoomType

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as RoomTypesController.cs
    participant H as Handler (Commands/Queries)
    participant R as RoomTypeRepository.cs
    participant DB as 💾 Database

    Note over CTL,R: GET /api/room-types
    C->>CTL: GET /api/room-types
    CTL->>H: GetRoomTypesQuery
    H->>R: repo.GetAllAsync()
    R->>DB: SELECT * FROM RoomTypes
    DB-->>H: List<RoomType>
    H-->>CTL: IEnumerable<RoomTypeDto>
    CTL-->>C: 200 OK [ { id, name, description }... ]

    Note over CTL,R: POST /api/room-types
    C->>CTL: POST { name, description }
    CTL->>H: CreateRoomTypeCommand
    Note over H: new RoomType { Name, Description }
    H->>R: repo.CreateAsync(entity)
    R->>DB: INSERT INTO RoomTypes
    CTL-->>C: 201 Created { id, name, description }

    Note over CTL,R: DELETE /api/room-types/{id}
    C->>CTL: DELETE /api/room-types/{id}
    CTL->>H: DeleteRoomTypeCommand(id)
    H->>R: repo.GetByIdAsync(id) → kiểm tra tồn tại
    H->>R: repo.DeleteAsync(id)
    R->>DB: ExecuteDeleteAsync (xóa vật lý)
    CTL-->>C: 204 No Content
```

---

## 4️⃣ API Quản lý Amenity (Tiện ích)

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as AmenitiesController.cs
    participant H as Handler (Commands/Queries)
    participant R as AmenityRepository.cs
    participant DB as 💾 Database

    Note over C,DB: GET /api/amenities
    C->>CTL: GET /api/amenities
    CTL->>H: GetAmenitiesQuery
    H->>R: repo.GetAllAsync()
    R->>DB: SELECT * FROM Amenities
    CTL-->>C: 200 OK [ { id, name, icon }... ]

    Note over C,DB: POST /api/amenities
    C->>CTL: POST { name: "Wifi", icon: "wifi-icon" }
    CTL->>H: CreateAmenityCommand
    Note over H: new Amenity { Name, Icon }
    H->>R: repo.CreateAsync(entity)
    R->>DB: INSERT INTO Amenities
    CTL-->>C: 201 Created { id, name, icon }

    Note over C,DB: PUT /api/amenities/{id}
    C->>CTL: PUT { name, icon }
    CTL->>H: UpdateAmenityCommand(id, name, icon)
    H->>R: GetByIdAsync → kiểm tra tồn tại
    Note over H: Set Name, Icon, UpdatedAt
    H->>R: UpdateAsync
    R->>DB: UPDATE Amenities SET ...
    CTL-->>C: 200 OK { id, name, icon }
```

---

## 5️⃣ API Upload ảnh (Cloudinary)

```mermaid
sequenceDiagram
    participant C as 🌐 Client
    participant CTL as UploadController.cs
    participant M as IMediator
    participant H as UploadImageHandler.cs
    participant S as CloudinaryService.cs
    participant CLD as ☁️ Cloudinary CDN

    C->>CTL: POST /api/upload/hotel/{hotelId}\nContent-Type: multipart/form-data\n[file binary]
    Note over CTL: UploadHotelImage(hotelId, IFormFile file)<br/>Gọi UploadFile(file, folder="hotels/{hotelId}")
    CTL->>M: mediator.Send(new UploadImageCommand(stream, fileName, folder))
    M->>H: Handle(UploadImageCommand)
    H->>S: cloudinary.UploadAsync(stream, fileName, folder)
    Note over S: Tạo ImageUploadParams<br/>{ File, Folder, UseFilename=true }
    S->>CLD: HTTP Upload to Cloudinary API
    CLD-->>S: { SecureUrl, PublicId }
    S-->>H: UploadResultDto(url, publicId)
    H-->>CTL: UploadResultDto
    CTL-->>C: 200 OK { url: "https://res.cloudinary.com/...", publicId: "hotels/abc/img123" }
```

---

## 📋 Bảng tóm tắt tất cả Endpoints

| Method | Endpoint | Controller | Handler | Repository | Return |
|--------|----------|------------|---------|------------|--------|
| GET | `/api/hotels` | HotelsController | GetHotelsHandler | HotelRepository | `PagedResult<HotelSummaryDto>` |
| GET | `/api/hotels/{id}` | HotelsController | GetHotelByIdHandler | HotelRepository | `HotelDto` |
| POST | `/api/hotels` | HotelsController | CreateHotelHandler | HotelRepository | `HotelDto` (201) |
| PUT | `/api/hotels/{id}` | HotelsController | UpdateHotelHandler | HotelRepository | `HotelDto` |
| DELETE | `/api/hotels/{id}` | HotelsController | DeleteHotelHandler | HotelRepository | `204 NoContent` |
| POST | `/api/hotels/{id}/amenities/{aid}` | HotelsController | AddHotelAmenityHandler | Amenity+HotelRepo | `204 NoContent` |
| DELETE | `/api/hotels/{id}/amenities/{aid}` | HotelsController | RemoveHotelAmenityHandler | Amenity+HotelRepo | `204 NoContent` |
| GET | `/api/hotels/{hotelId}/rooms` | RoomsController | GetRoomsByHotelHandler | RoomRepository | `IEnumerable<RoomSummaryDto>` |
| GET | `/api/hotels/{hotelId}/rooms/{id}` | RoomsController | GetRoomByIdHandler | RoomRepository | `RoomDto` |
| POST | `/api/hotels/{hotelId}/rooms` | RoomsController | CreateRoomHandler | Room+HotelRepo | `RoomDto` (201) |
| PUT | `/api/hotels/{hotelId}/rooms/{id}` | RoomsController | UpdateRoomHandler | RoomRepository | `RoomDto` |
| DELETE | `/api/hotels/{hotelId}/rooms/{id}` | RoomsController | DeleteRoomHandler | RoomRepository | `204 NoContent` |
| GET | `/api/room-types` | RoomTypesController | GetRoomTypesHandler | RoomTypeRepository | `IEnumerable<RoomTypeDto>` |
| GET | `/api/room-types/{id}` | RoomTypesController | GetRoomTypeByIdHandler | RoomTypeRepository | `RoomTypeDto` |
| POST | `/api/room-types` | RoomTypesController | CreateRoomTypeHandler | RoomTypeRepository | `RoomTypeDto` (201) |
| PUT | `/api/room-types/{id}` | RoomTypesController | UpdateRoomTypeHandler | RoomTypeRepository | `RoomTypeDto` |
| DELETE | `/api/room-types/{id}` | RoomTypesController | DeleteRoomTypeHandler | RoomTypeRepository | `204 NoContent` |
| GET | `/api/amenities` | AmenitiesController | GetAmenitiesHandler | AmenityRepository | `IEnumerable<AmenityDto>` |
| GET | `/api/amenities/{id}` | AmenitiesController | GetAmenityByIdHandler | AmenityRepository | `AmenityDto` |
| POST | `/api/amenities` | AmenitiesController | CreateAmenityHandler | AmenityRepository | `AmenityDto` (201) |
| PUT | `/api/amenities/{id}` | AmenitiesController | UpdateAmenityHandler | AmenityRepository | `AmenityDto` |
| DELETE | `/api/amenities/{id}` | AmenitiesController | DeleteAmenityHandler | AmenityRepository | `204 NoContent` |
| POST | `/api/upload/hotel/{hotelId}` | UploadController | UploadImageHandler | CloudinaryService | `UploadResultDto` |
| POST | `/api/upload/room/{roomId}` | UploadController | UploadImageHandler | CloudinaryService | `UploadResultDto` |

---

## 🔁 Flow chung (áp dụng cho tất cả API)

```mermaid
flowchart TD
    A["🌐 HTTP Request"] --> B["Controller\nvalidate route params\ngọi mediator.Send()"]
    B --> C{{"MediatR\ntìm Handler phù hợp"}}
    C --> D["Handler\nchứa business logic\ngọi Repository"]
    D --> E{Cần kiểm tra tồn tại?}
    E -->|Có| F["Repository.ExistsAsync()\nhoặc GetByIdAsync()"]
    F --> G{Tồn tại?}
    G -->|Không| H["throw NotFoundException\n→ 404 Not Found"]
    G -->|Có| I["Thực hiện thao tác\nCreate / Update / Delete"]
    E -->|Không| I
    I --> J["Repository gọi\nEF Core (DbContext)"]
    J --> K[("💾 Database")]
    K --> L["Trả về Entity"]
    L --> M["Handler map Entity\n→ DTO (record)"]
    M --> N["Controller trả về\nActionResult / IActionResult"]
    N --> O["🌐 JSON Response"]
```

---

> **Ghi chú thiết kế:**
> - **Soft Delete**: Hotel và Room không xóa vật lý, chỉ set `IsDeleted = true`. EF Core `HasQueryFilter` tự động lọc.
> - **NotFoundException**: Được throw từ Handler, sẽ được xử lý bởi `ExceptionMiddleware` để trả về 404.
> - **CQRS**: Commands (thay đổi dữ liệu) và Queries (đọc dữ liệu) tách biệt hoàn toàn.
> - **Nested Route**: Room nằm dưới Hotel (`/api/hotels/{hotelId}/rooms`) để thể hiện quan hệ sở hữu.
