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
5. Chức năng chính
Authentication
Đăng ký tài khoản khách hàng.
Đăng ký tài khoản tài xế.
Đăng nhập khách hàng.
Đăng nhập tài xế.
Cập nhật thông tin khách hàng.
Cập nhật thông tin tài xế.
Booking & Driver Matching
Tạo yêu cầu đặt xe.
Tìm tài xế phù hợp.
Phân công tài xế.
Tài xế chấp nhận hoặc từ chối chuyến.
Tìm tài xế tiếp theo khi bị từ chối hoặc không phản hồi.
Trip
Cập nhật trạng thái chuyến.
Cập nhật vị trí tài xế.
Theo dõi chuyến.
Xem lịch sử chuyến.
Fare & Payment
Tính cước chuyến đi.
Thanh toán tiền mặt.
Thanh toán điện tử.
Xử lý giao dịch thông qua Payment Provider.
Xử lý thanh toán thất bại.
Notification & Rating
Gửi thông báo.
Thông báo khi không tìm được tài xế.
Thông báo kết quả thanh toán.
Khách hàng đánh giá tài xế.
Operation
Quản lý khách hàng.
Quản lý tài xế.
Quản lý phương tiện.
Quản lý chuyến đi.
Tra cứu giao dịch.
Xử lý chuyến bị lỗi.
Xem báo cáo hoạt động.
6. API Documentation

Các API được tổ chức theo từng nhóm nghiệp vụ:

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
