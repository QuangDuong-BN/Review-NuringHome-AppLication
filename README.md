# Ứng Dụng Đa Nền Tảng Cho Trung Tâm Dưỡng Lão

## Liên Kết Dự Án

- [NursingHome Backend - Service 1](https://github.com/QuangDuong-BN/NursingHome-Backend)
- [Notification Service - Service 2](https://github.com/QuangDuong-BN/notification-service)
- [Nursinghome Api Gateway](https://github.com/QuangDuong-BN/nursing-home-api-gateway)
- [Android Native App](https://github.com/QuangDuong-BN/NursingHome-FE-Android)

## Giới Thiệu Dự Án

Ứng dụng đa nền tảng này được phát triển để hỗ trợ các trung tâm dưỡng lão, giúp người nhà dễ dàng theo dõi tình trạng sức khỏe của người thân, đặt lịch dịch vụ chăm sóc, và kết nối với nhân viên phụ trách qua các tính năng gọi thoại và video. Ngoài ra, ứng dụng còn tích hợp hệ thống quản lý dành cho nhân viên để theo dõi và điều phối các yêu cầu dịch vụ.

Dự án bao gồm một **ứng dụng di động** cho người dùng và một **website quản lý** cho nhân viên, với khả năng giao tiếp giữa các microservices thông qua các API backend. Ứng dụng sử dụng Redis để quản lý phiên đăng nhập và OTP, kết hợp với Kafka cho giao tiếp giữa các dịch vụ.

## Công Nghệ Sử Dụng

**Mô Hình**: Microservices

**Backend**: 
- Spring Boot
- Spring Data JPA
- Spring Security

**Frontend**: 
- HTML, CSS, JavaScript, Bootstrap

**Android**: 
- Android Native (Java)

**DBMS**: 
- MySQL

**Công Nghệ Khác**: 
- Redis
- Kafka
- Spring Cloud

### **Redis**

- Hệ thống triển khai **Token Versioning** để quản lý JWT, lưu trữ phiên bản token trong **Redis** và **Database**.  
- Redis kết hợp cơ chế **TTL (Time-To-Live)** để quản lý blacklist token và mã OTP một cách hiệu quả. Các token bị thu hồi được lưu trong Redis với TTL tương ứng thời gian hết hạn, đảm bảo tự động xóa khi không còn cần thiết.  
- Tương tự, mã OTP được lưu trữ trong Redis với TTL ngắn (ví dụ: 5 phút), đảm bảo mã chỉ có hiệu lực trong thời gian quy định và tự động xóa sau khi hết hạn.

### **Kafka**

- Các service trong hệ thống giao tiếp với **Notification Service** thông qua Kafka để sử dụng tính năng gửi email. Kafka giúp việc gửi email giữa các microservices diễn ra hiệu quả, hỗ trợ việc xử lý bất đồng bộ và đảm bảo tính mở rộng của hệ thống.


## Phân Tích Thiết Kế Hệ Thông
![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/usecase.png)
> *Biều đồ Use Case tổng quát.*

![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/database.png)
> *Biểu đồ cơ sở dữ liệu.*

![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/tuantu1.png)
> *Biểu đồ tuần tự đăng kí sản phẩm dịch vụ.*

![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/tuantu2.png)
> *Biểu đồ tuần tự đăng kí lịch thăm người thân.*
## Hình Ảnh Ứng Dụng

### Giao Diện Ứng Dụng Di Động

![Giao diện ứng dụng di động 1](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image1.png)
![Giao diện ứng dụng di động 2](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image2.png)
![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image3.png)


> *Hình ảnh trên mô tả các giao diện chính của ứng dụng di động, bao gồm việc đặt lịch dịch vụ, theo dõi sức khỏe và gọi điện/video với nhân viên.*

![Giao diện ứng dụng di động 1](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image5.png)
![Giao diện ứng dụng di động 2](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image6.png)
![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image7.png)


> *Giao diện theo dõi hoạt động, đặt lịch thăm và lịch sử đặt lịch thăm*

![Giao diện ứng dụng di động 1](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image8.png)
![Giao diện ứng dụng di động 2](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image9.png)
![Giao diện ứng dụng di động 3](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image10.png)


> *Giao diện liên lạc*

### Giao Diện Website Quản Lý Nhân Viên

![Giao diện website quản lý](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image4.png)

> *Hình ảnh trên mô tả giao diện website quản lý của nhân viên, nơi họ có thể theo dõi và điều phối các yêu cầu dịch vụ, đồng thời quản lý các hoạt động của trung tâm dưỡng lão.*

## Các Tính Năng Nổi Bật

- **Đặt Dịch Vụ**: Người dùng có thể dễ dàng đặt dịch vụ chăm sóc cho người thân, theo dõi tình trạng sức khỏe và nhận thông báo.
- **Gọi Thoại và Video**: Tính năng gọi thoại và video trực tiếp giữa người dùng và nhân viên chăm sóc.
- **Quản Lý Nhân Viên**: Nhân viên có thể quản lý và theo dõi các yêu cầu, tình trạng sức khỏe của người dùng qua website.
- **Bảo Mật và Quản Lý Phiên Đăng Nhập**: Sử dụng Redis và Token Versioning để quản lý đăng nhập và bảo mật cho người dùng.

## Kết Luận

Ứng dụng này mang lại giải pháp tiện lợi và hiệu quả cho các trung tâm dưỡng lão, giúp người nhà dễ dàng chăm sóc và theo dõi người thân, đồng thời hỗ trợ nhân viên quản lý công việc một cách dễ dàng và nhanh chóng.

