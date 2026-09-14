# CAB SYSTEM – Service-Oriented Programming

## 1. Giới thiệu

**CAB SYSTEM** là hệ thống quản lý và đặt xe được xây dựng theo định hướng **Service-Oriented Architecture (SOA)**.

Hệ thống hỗ trợ khách hàng đặt xe, tìm và phân công tài xế, theo dõi và thực hiện chuyến đi, tính cước, thanh toán và đánh giá tài xế. Đồng thời, hệ thống cung cấp các chức năng quản lý khách hàng, tài xế, phương tiện, chuyến đi, giao dịch, xử lý chuyến lỗi và báo cáo hoạt động.

## 2. Mục tiêu

- Hỗ trợ quy trình đặt và thực hiện chuyến xe.
- Tự động tìm kiếm và phân công tài xế phù hợp.
- Hỗ trợ thanh toán tiền mặt và thanh toán điện tử.
- Quản lý thông tin khách hàng, tài xế, phương tiện và chuyến đi.
- Theo dõi lịch sử chuyến và giao dịch.
- Cung cấp thông báo và đánh giá tài xế.
- Hỗ trợ nhân viên vận hành quản lý và theo dõi hoạt động của hệ thống.

## 3. Đối tượng sử dụng

| Actor | Vai trò |
|---|---|
| **Customer** | Đăng ký, đăng nhập, đặt xe, theo dõi chuyến, thanh toán, xem lịch sử và đánh giá tài xế. |
| **Driver** | Đăng ký, đăng nhập, cập nhật thông tin, cập nhật vị trí, nhận/chấp nhận/từ chối chuyến và cập nhật trạng thái chuyến. |
| **Operation Staff** | Quản lý khách hàng, tài xế, phương tiện, chuyến đi, giao dịch và xử lý chuyến lỗi. |
| **Management** | Theo dõi và xem báo cáo hoạt động của hệ thống. |
| **Payment Provider** | Xử lý các giao dịch thanh toán điện tử. |
| **Notification Provider** | Hỗ trợ gửi thông báo đến người dùng. |

## 4. Quy trình chính

```text
Đăng nhập
    ↓
Đặt xe
    ↓
Tìm & phân công tài xế
    ↓
Chấp nhận / từ chối chuyến
    ↓
Thực hiện chuyến
    ↓
Hoàn thành
    ↓
Tính cước
    ↓
Thanh toán
    ↓
Xử lý thanh toán điện tử (nếu có)
```
## 5. Các chức năng chính

### 5.1. Quản lý tài khoản

- Đăng ký tài khoản khách hàng.
- Đăng ký tài khoản tài xế.
- Đăng nhập.
- Cập nhật thông tin cá nhân.
- Tài xế cập nhật thông tin phương tiện và trạng thái hoạt động.

### 5.2. Đặt xe và phân công tài xế

- Nhập điểm đón.
- Nhập điểm đến.
- Lựa chọn loại xe.
- Tạo yêu cầu đặt xe.
- Tìm tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và tiêu chí vận hành.
- Phân công tài xế.
- Tìm tài xế tiếp theo khi tài xế từ chối hoặc không phản hồi.
- Thông báo khi không tìm được tài xế.

### 5.3. Quản lý chuyến đi

- Tài xế chấp nhận hoặc từ chối chuyến.
- Cập nhật trạng thái chuyến.
- Cập nhật vị trí tài xế.
- Khách hàng theo dõi trạng thái chuyến.
- Ghi nhận chuyến hoàn thành.
- Xem lịch sử chuyến.

### 5.4. Tính cước và thanh toán

- Xác định số tiền khách hàng phải trả.
- Thanh toán bằng tiền mặt.
- Thanh toán điện tử.
- Tích hợp với Payment Provider.
- Bảo vệ dữ liệu thanh toán.
- Xử lý trường hợp thanh toán thất bại.

### 5.5. Thông báo và đánh giá

- Gửi thông báo đến khách hàng và tài xế.
- Thông báo khi không tìm được tài xế.
- Thông báo kết quả thanh toán.
- Khách hàng đánh giá tài xế sau chuyến đi.

### 5.6. Quản lý vận hành

- Quản lý khách hàng.
- Quản lý tài xế.
- Quản lý phương tiện.
- Quản lý chuyến đi.
- Tra cứu giao dịch.
- Xử lý chuyến bị lỗi.
- Xem báo cáo hoạt động.

## 6. Cấu trúc API

Các API được phân chia theo từng nhóm nghiệp vụ:

```text
API/
├── authentication/
├── booking/
├── driver-location/
├── driver-matching/
├── driver-response/
├── fare/
├── notification/
├── operation/
├── payment/
├── rating/
├── report/
├── trip/
├── trip-history/
└── trip-tracking/
