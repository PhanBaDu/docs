# 7. NON-FUNCTIONAL REQUIREMENTS AND OTHERS

## Performance

| No. | Requirement |
|-----|-------------|
| 1 | Hệ thống phải hỗ trợ tối thiểu 1000 người dùng truy cập đồng thời mà không ảnh hưởng đến hiệu suất. Tiêu chí: Stress test với 1000 concurrent users, response time < 500ms, error rate < 1% |
| 2 | Thời gian phản hồi API trung bình phải dưới 200ms cho các thao tác đơn giản (xem sách, giỏ hàng, tìm kiếm). Tiêu chí: 95% requests < 200ms, 99% requests < 500ms |
| 3 | Thời gian tải trang không vượt quá 3 giây với kết nối internet tốc độ trung bình. Tiêu chí: Lighthouse Performance score ≥ 80, First Contentful Paint < 1.5s |
| 4 | Thời gian xử lý thanh toán và đặt hàng không vượt quá 5 giây. Tiêu chí: 95% checkout transactions hoàn thành trong 5 giây |
| 5 | Real-time chat hỗ trợ khách hàng có độ trễ tối đa 1 giây (sử dụng Socket.IO). Tiêu chí: Message latency < 1s với 500 concurrent connections |
| 6 | Tính năng "đọc thử" sách phải tải nhanh với độ trễ tối đa 2 giây. Tiêu chí: PDF/preview loading time < 2s, CDN cache hit rate > 80% |

## Scalability

| No. | Requirement |
|-----|-------------|
| 1 | Database PostgreSQL phải có khả năng lưu trữ tối thiểu 50,000 đầu sách và 100,000 khách hàng |
| 2 | Hệ thống phải xử lý được ít nhất 2,000 đơn hàng mỗi ngày (bao gồm đơn online và offline). Tiêu chí: Load test 2000+ orders/day, peak load 200 orders/hour |
| 3 | Cho phép nhiều nhân viên (Admin, Nhân viên bán hàng, Nhân viên kho) đồng thời quản lý đơn hàng, cập nhật sách mà không xung đột dữ liệu. Implement optimistic locking hoặc version control |
| 4 | Hỗ trợ upload và lưu trữ tối thiểu 100,000 hình ảnh sách (bìa sách, ảnh chi tiết, ảnh đọc thử) và 50,000 ảnh/video từ đánh giá người dùng. Sử dụng CDN, image optimization (WebP, lazy loading) |
| 5 | Kiến trúc hệ thống phải cho phép mở rộng horizontal scaling khi lượng truy cập tăng. Thiết kế stateless backend, load balancer, container orchestration (Docker + Kubernetes). Auto-scaling rule: khi CPU > 70% thì scale thêm 1 instance, maximum 10 instances |
| 6 | Hỗ trợ đồng bộ dữ liệu thời gian thực giữa kênh online và offline. Tiêu chí: Sync delay < 5 giây, có conflict resolution mechanism |

## Security

| No. | Requirement |
|-----|-------------|
| 1 | Backend sử dụng Node.js phiên bản 20.0 trở lên để đảm bảo các bản vá bảo mật mới nhất. Thực hiện dependency audit hàng tuần |
| 2 | Xác thực người dùng bắt buộc sử dụng JWT (JSON Web Token) với thời gian hết hạn 24 giờ. Có cơ chế refresh token |
| 3 | Mật khẩu người dùng phải được mã hóa bằng Bcrypt với salt rounds tối thiểu là 10 |
| 4 | Phân quyền rõ ràng giữa 4 vai trò: Admin, Nhân viên bán hàng, Nhân viên kho và Khách hàng - mỗi vai trò chỉ truy cập được các chức năng được phép. Implement RBAC (Role-Based Access Control) |
| 5 | Tích hợp các cổng thanh toán (VNPay, MoMo, ZaloPay, Viettel Money) phải tuân thủ chuẩn bảo mật PCI DSS. Không lưu trữ thông tin thẻ, sử dụng tokenization |
| 6 | Dữ liệu hệ thống (thông tin sách, đơn hàng, khách hàng, tồn kho) được sao lưu tự động hàng ngày và lưu trữ tại server backup riêng biệt. Retention policy: lưu backup 90 ngày. Thực hiện backup restoration test mỗi quý. RPO < 24 giờ, RTO < 6 giờ |
| 7 | Tất cả API endpoints phải được bảo vệ bởi middleware xác thực (Passport.js). API security audit với test coverage 100% |
| 8 | Sử dụng HTTPS/SSL cho mọi kết nối giữa client và server. Enable security headers (HSTS, X-Frame-Options) |
| 9 | Implement CORS policy để chỉ cho phép các domain được phê duyệt truy cập API |
| 10 | Chống tấn công XSS, SQL Injection, CSRF thông qua validation (Zod) và sanitization dữ liệu đầu vào. Thực hiện penetration test mỗi 6 tháng hoặc sau mỗi major update. Tuân thủ OWASP Top 10 |
| 11 | Bảo mật thông tin khách hàng (họ tên, số điện thoại, địa chỉ, lịch sử mua hàng) tuân thủ Nghị định 13/2023 về bảo vệ dữ liệu cá nhân và GDPR principles cho khách hàng quốc tế. Data encryption at rest |
| 12 | Khôi phục mật khẩu thông qua email/SMS phải có cơ chế xác thực OTP với thời gian hết hạn 5 phút. Có rate limiting để chống spam |
| 13 | Audit trail cho các thao tác đặc biệt (xóa sách/đơn hàng, sửa giá, thay đổi tồn kho, hoàn tiền). Log phải ghi: timestamp, user, action, old value, new value. Retention: 1 năm. Có chức năng export log cho audit |

## Browser

| No. | Requirement |
|-----|-------------|
| 1 | Hỗ trợ các trình duyệt hiện đại: Chrome (3 phiên bản gần nhất - từ version 120 trở lên), Firefox (3 phiên bản gần nhất - từ version 121 trở lên). Có browser compatibility matrix và test plan |
| 2 | Hỗ trợ Microsoft Edge (phiên bản dựa trên Chromium, từ version 120 trở lên) |
| 3 | Hỗ trợ Safari 14 trở lên (cho người dùng macOS và iOS) |
| 4 | Responsive design tương thích với các thiết bị mobile (iOS 15+, Android 10+) cho cả khách hàng và nhân viên. Test các viewport: mobile 375px-767px, tablet 768px-1023px, desktop 1024px+ |
| 5 | Không hỗ trợ Internet Explorer (đã ngừng hỗ trợ từ Microsoft). Hiển thị thông báo deprecation cho IE users |
| 6 | Giao diện tối ưu cho màn hình tablet để nhân viên bán hàng dễ dàng xử lý đơn hàng tại quầy |

## Reliability

| No. | Requirement |
|-----|-------------|
| 1 | Uptime hệ thống đạt tối thiểu 99.5% trong tháng (cho phép downtime không quá 3.6 giờ/tháng). Implement uptime monitoring (Pingdom/UptimeRobot). Thực hiện DR (Disaster Recovery) drill mỗi 6 tháng. RPO < 2 giờ, RTO < 6 giờ |
| 2 | Thời gian phục hồi hệ thống từ dữ liệu backup trong trường hợp sự cố không quá 6 giờ. Có documented recovery procedures và quarterly DR test |
| 3 | Cơ chế retry tự động cho các giao dịch thanh toán thất bại. Implement exponential backoff, maximum 3 retries |
| 4 | Đồng bộ dữ liệu tồn kho giữa online và offline phải chính xác 100% để tránh bán quá số lượng có sẵn. Có conflict resolution mechanism và real-time stock validation |
| 5 | Thông báo trạng thái đơn hàng cho khách hàng phải được gửi kịp thời (độ trễ tối đa 30 giây). Sử dụng message queue (RabbitMQ/Redis) |
| 6 | Hệ thống báo cáo phải luôn sẵn sàng cho Admin và nhân viên truy cập mọi lúc. Implement caching strategy cho reports |

## Availability

| No. | Requirement |
|-----|-------------|
| 1 | Database và Backend phải có cơ chế high-availability. Deploy theo mô hình active-active hoặc active-standby, multi-zone setup cho database, health check cho backend services, automatic failover < 30 giây |
| 2 | Critical APIs (checkout, payment, inventory check) phải có availability > 99.9%. Monitoring riêng cho critical endpoints, implement circuit breaker pattern, graceful degradation khi service phụ fail |

## Maintainability

| No. | Requirement |
|-----|-------------|
| 1 | Code phải tuân thủ coding standards và best practices. Setup ESLint/Prettier, code review process bắt buộc, SonarQube quality gate score > 80% |
| 2 | CI/CD pipeline cho automated testing và deployment. Setup GitHub Actions/GitLab CI, automated test coverage > 70%, deployment automation với rollback capability |
| 3 | Comprehensive documentation: API documentation (Swagger/OpenAPI), system architecture diagrams (C4 model), deployment guide, onboarding guide cho developer mới |

## Compliance

| No. | Requirement |
|-----|-------------|
| 1 | Tuân thủ Nghị định 13/2023 về bảo vệ dữ liệu cá nhân Việt Nam. Có privacy policy page, consent mechanism, data subject rights (access/delete/export data), data retention policy rõ ràng |
| 2 | Tuân thủ quy định về hóa đơn điện tử theo quy định của Tổng cục Thuế (nếu doanh nghiệp đủ điều kiện). Tích hợp hệ thống hóa đơn điện tử nếu cần |
| 3 | Lưu trữ transaction logs phục vụ audit và pháp lý. Retention: 5 năm theo quy định kế toán. Implement tamper-proof logging |

## Usability

| No. | Requirement |
|-----|-------------|
| 1 | Thời gian học sử dụng hệ thống cho nhân viên mới < 3 giờ đào tạo. Cung cấp user training document và video tutorials. Sau 3 giờ, nhân viên có thể: tạo đơn hàng, xử lý thanh toán, cập nhật tồn kho |
| 2 | Người dùng có thể hoàn thành task chính (đặt hàng online) trong < 3 phút và ≤ 5 bước. Thực hiện usability test với ít nhất 5 users, đo task completion time |
| 3 | Accessibility compliance level AA theo WCAG 2.0. Support keyboard navigation, screen reader compatible, color contrast ratio > 4.5:1, alt text cho tất cả images |

## Interfaces

| No. | Requirement |
|-----|-------------|
| 1 | Sử dụng Framework Next.js (version 14+) để tạo giao diện người dùng với SSR/SSG optimization |
| 2 | Styling sử dụng Tailwind CSS kết hợp shadcn/ui components. Có consistent design system |
| 3 | Hỗ trợ đa ngôn ngữ (Tiếng Việt, Tiếng Anh) thông qua next-intl. 100% content được dịch, có language switcher |
| 4 | Responsive design tương thích mọi kích thước màn hình: mobile (375px-767px), tablet (768px-1023px), desktop (1024px+) |
| 5 | Giao diện riêng biệt cho từng vai trò: Admin Dashboard, Staff POS Interface, Warehouse Management UI, Customer Shopping Interface. Role-based UI và navigation |
| 6 | Dashboard trực quan cho Admin để theo dõi doanh thu, tồn kho, đơn hàng theo thời gian thực. Sử dụng charts (Recharts), auto-refresh data mỗi 30 giây |
| 7 | Giao diện POS (Point of Sale) đơn giản, nhanh cho nhân viên bán hàng tại quầy. Optimize cho tablet, tích hợp barcode scanner, quick checkout flow |
| 8 | Tích hợp API đơn vị vận chuyển (GHTK, GHN, J&T Express) để theo dõi đơn hàng. Sync tracking number, webhook handling cho status updates |

## Assumptions

| No. | Assumption |
|-----|------------|
| 1 | Có thể tạm ngưng hệ thống nếu cần phải nâng cấp (thời gian bảo trì: 2-4h sáng, thông báo trước 24 giờ) |
| 2 | Người dùng (khách hàng và nhân viên) có kết nối internet ổn định tối thiểu 5 Mbps |
| 3 | Admin và nhân viên (bán hàng, kho) được đào tạo cơ bản trước khi vận hành hệ thống |
| 4 | Môi trường dev, staging, production được tách biệt hoàn toàn |
| 5 | Nhà sách có sẵn thiết bị (máy tính, máy quét mã vạch, máy in hóa đơn) để vận hành hệ thống |
| 6 | Khách hàng có tài khoản ngân hàng hoặc ví điện tử để thanh toán online |
| 7 | Thông tin sách (tên, tác giả, NXB, giá) được nhập chính xác bởi nhân viên kho |
| 8 | Hệ thống xếp hạng (ranking) khách hàng được cập nhật tự động dựa trên tổng giá trị chi tiêu |
