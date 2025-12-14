# 7. Availability (Tính Khả Dụng)

## 7.1. Mục Tiêu Availability

### 7.1.1. Uptime Requirements
- **Target Uptime**: 99.5% (tương đương ~3.6 giờ downtime/tháng)
- **Planned Downtime**: ≤ 2 giờ/tháng cho bảo trì
- **Unplanned Downtime**: ≤ 1.6 giờ/tháng
- **Recovery Time Objective (RTO)**: ≤ 30 phút
- **Recovery Point Objective (RPO)**: ≤ 24 giờ

### 7.1.2. Service Level Objectives (SLOs)
| Dịch vụ | Availability Target | Downtime cho phép/tháng |
|---------|-------------------|------------------------|
| Core API | 99.5% | 3.6 giờ |
| Admin Portal | 99.0% | 7.2 giờ |
| Database | 99.9% | 43 phút |
| File Storage | 99.5% | 3.6 giờ |

## 7.2. Backup Strategy

### 7.2.1. Database Backup
**Automated Daily Backup:**
- **Thời gian**: 2:00 AM - 4:00 AM (giờ thấp điểm)
- **Loại**: Full backup hàng ngày
- **Retention**: 
  - Daily backups: 7 ngày
  - Weekly backups: 4 tuần
  - Monthly backups: 12 tháng
- **Storage**: Cloud storage với geo-redundancy

**Incremental Backup:**
- **Tần suất**: Mỗi 6 giờ
- **Retention**: 48 giờ
- **Mục đích**: Giảm RPO xuống còn 6 giờ

### 7.2.2. File Storage Backup
- **Tần suất**: Daily backup tại 3:00 AM
- **Phương pháp**: Incremental backup
- **Retention**: 30 ngày
- **Verification**: Weekly restore test

### 7.2.3. Configuration Backup
- **Source Code**: Git repository với multiple remotes
- **Configuration Files**: Version controlled, backed up daily
- **Secrets**: Encrypted backup trong vault system
- **Retention**: Indefinite cho configs quan trọng

### 7.2.4. Backup Testing
- **Restore Test**: Monthly full restore test
- **Disaster Recovery Drill**: Quarterly
- **Documentation**: Cập nhật runbook sau mỗi test

## 7.3. Maintenance Windows

### 7.3.1. Planned Maintenance
- **Thời gian**: Chủ nhật, 1:00 AM - 3:00 AM
- **Tần suất**: 2 lần/tháng (tối đa)
- **Thông báo**: 72 giờ trước cho users
- **Rollback Plan**: Sẵn sàng cho mọi deployment

### 7.3.2. Emergency Maintenance
- **Approval**: CTO/Tech Lead
- **Notification**: Ngay lập tức qua email/SMS
- **Maximum Duration**: 2 giờ
- **Post-mortem**: Bắt buộc trong vòng 24 giờ

## 7.4. High Availability Measures

### 7.4.1. Infrastructure
- **Load Balancer**: Active-active configuration
- **Application Servers**: Minimum 2 instances
- **Database**: Primary-replica setup với automatic failover
- **Cache**: Redis cluster với sentinel

### 7.4.2. Monitoring & Alerting
- **Health Checks**: Every 30 seconds
- **Alert Response Time**: < 5 phút
- **On-call Rotation**: 24/7 coverage
- **Escalation**: Automatic sau 15 phút

### 7.4.3. Degraded Mode
Khi một số services không khả dụng:
- **Read-only mode**: Cho phép xem dữ liệu
- **Cached responses**: Sử dụng cache khi DB down
- **Queue requests**: Lưu requests để xử lý sau

---

# 8. Maintainability (Tính Bảo Trì)

## 8.1. Code Quality Standards

### 8.1.1. Test Coverage Requirements
**Minimum Coverage:**
- **Unit Tests**: ≥ 80% coverage
- **Integration Tests**: ≥ 60% coverage
- **Critical Paths**: 100% coverage
- **New Code**: ≥ 85% coverage (không được giảm tổng coverage)

**Coverage Tools:**
- **Backend**: Jest/pytest với coverage reports
- **Frontend**: Jest + React Testing Library
- **CI/CD**: Automated coverage checks, fail build nếu < 80%

### 8.1.2. Code Review Guidelines
**Mandatory Reviews:**
- Tối thiểu 1 reviewer cho mọi PR
- 2 reviewers cho critical components
- Tech Lead approval cho architectural changes

**Review Checklist:**
- [ ] Code follows style guide
- [ ] Tests included và pass
- [ ] No security vulnerabilities
- [ ] Documentation updated
- [ ] Performance impact assessed
- [ ] Backward compatibility maintained

### 8.1.3. Coding Standards
**Style Guides:**
- **JavaScript/TypeScript**: Airbnb style guide + ESLint
- **Python**: PEP 8 + Black formatter
- **SQL**: SQL Style Guide
- **Enforcement**: Pre-commit hooks + CI checks

## 8.2. Refactoring Guidelines

### 8.2.1. Khi Nào Refactor
**Triggers:**
- Technical debt score > threshold
- Code complexity metrics (cyclomatic complexity > 10)
- Duplicate code > 3 lần
- Performance bottlenecks identified
- Before adding new features to legacy code

### 8.2.2. Refactoring Process
**Steps:**
1. **Document**: Ghi chép current behavior
2. **Tests**: Đảm bảo test coverage ≥ 80% trước refactor
3. **Small Changes**: Incremental refactoring
4. **Verify**: Run full test suite sau mỗi change
5. **Review**: Code review bắt buộc
6. **Deploy**: Canary deployment

**Safe Refactoring Practices:**
- Không thay đổi public APIs mà không deprecation notice
- Maintain backward compatibility tối thiểu 2 versions
- Feature flags cho changes lớn
- Automated tests chạy liên tục

### 8.2.3. Technical Debt Management
**Tracking:**
- Label PRs với "tech-debt" tag
- Monthly tech debt review meeting
- Allocate 20% sprint capacity cho tech debt

**Prioritization:**
- **P0 (Critical)**: Security issues, data corruption risks
- **P1 (High)**: Performance issues, scalability blockers  
- **P2 (Medium)**: Code smell, maintainability issues
- **P3 (Low)**: Nice-to-have improvements

## 8.3. Documentation Standards

### 8.3.1. Code Documentation
**Required:**
- **Functions**: JSDoc/docstring cho public functions
- **Classes**: Purpose, usage examples
- **Complex Logic**: Inline comments giải thích "why"
- **APIs**: OpenAPI/Swagger specs

### 8.3.2. System Documentation
**Living Documents:**
- **Architecture Decision Records (ADRs)**: Cho mọi major decisions
- **Runbooks**: Deployment, troubleshooting procedures
- **API Documentation**: Auto-generated + updated với mỗi release
- **Changelog**: Semantic versioning với detailed notes

**Update Frequency:**
- ADRs: Khi có architectural changes
- Runbooks: Sau mỗi incident/deployment
- API docs: Automated với mỗi deployment
- README: Cập nhật với feature changes

## 8.4. Dependency Management

### 8.4.1. Version Control
- **Lock Files**: Commit package-lock.json, yarn.lock, requirements.txt
- **Automated Updates**: Dependabot/Renovate cho security patches
- **Version Pinning**: Major versions pinned, minor/patch flexible
- **Audit**: Monthly security audit của dependencies

### 8.4.2. Deprecation Policy
**Process:**
1. **Announce**: Deprecation notice 3 months trước
2. **Document**: Migration guide
3. **Support**: Maintain old version trong deprecation period
4. **Remove**: Sau 6 months, remove deprecated code

## 8.5. Monitoring & Observability

### 8.5.1. Logging Standards
**Log Levels:**
- **ERROR**: System errors requiring immediate action
- **WARN**: Potential issues, degraded performance
- **INFO**: Important business events
- **DEBUG**: Detailed diagnostic information

**Structured Logging:**
- JSON format với consistent fields
- Request ID tracing across services
- User context (sanitized)
- Retention: 30 ngày hot, 90 ngày cold storage

### 8.5.2. Metrics Collection
**Key Metrics:**
- Response time (p50, p95, p99)
- Error rates by endpoint
- Database query performance
- Cache hit rates
- Business metrics (orders, revenue, etc.)

**Dashboards:**
- System health dashboard (24/7 monitoring)
- Business metrics dashboard
- Per-service dashboards
- Custom alerts cho anomalies

## 8.6. Development Workflow

### 8.6.1. Git Workflow
- **Branching**: GitFlow (main, develop, feature/*, hotfix/*)
- **Commits**: Conventional commits (feat, fix, docs, refactor, etc.)
- **PRs**: Template với checklist
- **Protected Branches**: main, develop require reviews

### 8.6.2. CI/CD Pipeline
**Automated Checks:**
- Linting & formatting
- Unit tests + coverage check (≥80%)
- Integration tests
- Security scanning (Snyk, SonarQube)
- Build verification
- Automated deployment to staging

**Quality Gates:**
- All tests pass
- Coverage ≥ 80%
- No critical security vulnerabilities
- No code smells severity > Major
- Performance regression check

---

## Summary Checklist

### Availability ✓
- [x] Backup strategy defined (daily, retention policy)
- [x] Downtime limit: ≤ 2h/tháng planned maintenance
- [x] RTO/RPO defined
- [x] High availability measures documented
- [x] Monitoring and alerting setup

### Maintainability ✓
- [x] Code coverage requirement: ≥ 80%
- [x] Refactoring guidelines established
- [x] Documentation standards defined
- [x] Code review process documented
- [x] Tech debt management process
- [x] CI/CD quality gates configured
