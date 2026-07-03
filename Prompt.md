# Prompt sinh mã nguồn API Spring Boot từ tài liệu SRS

## Vai trò

Bạn là Senior Backend Developer có kinh nghiệm Java 17, Spring Boot, Spring Data JPA và thiết kế RESTful API.

## Bối cảnh

Dựa trên tài liệu SRS eKYC của ABC Bank, hãy sinh mã nguồn cho chức năng:

"Đăng ký mở tài khoản cơ bản"

## Mô tả chức năng từ SRS

Khách hàng nhập thông tin đăng ký gồm:

- fullName
- phone
- email
- citizenId

Hệ thống kiểm tra dữ liệu hợp lệ, tạo hồ sơ tài khoản mới với trạng thái ban đầu là PENDING.

Sau khi tạo thành công, hệ thống trả về:

- accountId
- accountNumber
- status

Status gồm:

- PENDING
- ACTIVE

## Yêu cầu sinh code

Hãy sinh đầy đủ mã nguồn Spring Boot theo mô hình MVC 3 lớp:

- Entity
- DTO Request
- DTO Response
- Repository
- Service Interface
- Service Implementation
- Controller
- Enum AccountStatus
- Custom validation citizenId 12 số
- Exception xử lý lỗi cơ bản

## Công nghệ bắt buộc

- Java 17
- Spring Boot
- Spring Web
- Spring Data JPA
- Validation
- MySQL hoặc H2 Database

## Yêu cầu chất lượng code

- Có JavaDoc cho class và method.
- Có comment tiếng Việt trong các đoạn xử lý logic.
- Sử dụng Data Validation:
  - @NotBlank cho fullName, phone, citizenId
  - @Email cho email
  - Custom validation cho citizenId đúng 12 chữ số
- API endpoint:

POST /api/accounts/register

## Bonus

Sinh thêm Architecture Diagram bằng Mermaid mô tả luồng:

Client -> Controller -> Service -> Repository -> Database

## Định dạng trả lời

Trình bày theo từng file code rõ ràng.

Không bỏ sót class.