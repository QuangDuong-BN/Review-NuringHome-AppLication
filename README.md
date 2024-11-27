# Ứng Dụng Đa Nền Tảng Cho Trung Tâm Dưỡng Lão

## Liên Kết Dự Án

- [Backend - Service 1](http://link-to-backend-service-1)
- [Backend - Service 2](http://link-to-backend-service-2)
- [Backend - Service 3](http://link-to-backend-service-3)
- [Android Native App](http://link-to-android-native-app)

## Giới Thiệu Dự Án

Ứng dụng đa nền tảng này được phát triển để hỗ trợ các trung tâm dưỡng lão, giúp người nhà dễ dàng theo dõi tình trạng sức khỏe của người thân, đặt lịch dịch vụ chăm sóc, và kết nối với nhân viên phụ trách qua các tính năng gọi thoại và video. Ngoài ra, ứng dụng còn tích hợp hệ thống quản lý dành cho nhân viên để theo dõi và điều phối các yêu cầu dịch vụ.

Dự án bao gồm một **ứng dụng di động** cho người dùng và một **website quản lý** cho nhân viên, với khả năng giao tiếp giữa các microservices thông qua các API backend. Ứng dụng sử dụng Redis để quản lý phiên đăng nhập và OTP, kết hợp với Kafka cho giao tiếp giữa các dịch vụ.

## Hình Ảnh Ứng Dụng

### Giao Diện Ứng Dụng Di Động

![Giao diện ứng dụng di động 1]([image1.jpg](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image1.png))
![Giao diện ứng dụng di động 2]([image2.jpg](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image2.png))
![Giao diện ứng dụng di động 3]([gimage3.jp](https://github.com/QuangDuong-BN/save-image-for-repo/blob/main/nursinghome/image3.png))

> *Hình ảnh trên mô tả các giao diện chính của ứng dụng di động, bao gồm việc đặt lịch dịch vụ, theo dõi sức khỏe và gọi điện/video với nhân viên.*

### Giao Diện Website Quản Lý Nhân Viên

![Giao diện website quản lý](image4.jpg)

> *Hình ảnh trên mô tả giao diện website quản lý của nhân viên, nơi họ có thể theo dõi và điều phối các yêu cầu dịch vụ, đồng thời quản lý các hoạt động của trung tâm dưỡng lão.*

## Các Tính Năng Nổi Bật

- **Đặt Dịch Vụ**: Người dùng có thể dễ dàng đặt dịch vụ chăm sóc cho người thân, theo dõi tình trạng sức khỏe và nhận thông báo.
- **Gọi Thoại và Video**: Tính năng gọi thoại và video trực tiếp giữa người dùng và nhân viên chăm sóc.
- **Quản Lý Nhân Viên**: Nhân viên có thể quản lý và theo dõi các yêu cầu, tình trạng sức khỏe của người dùng qua website.
- **Bảo Mật và Quản Lý Phiên Đăng Nhập**: Sử dụng Redis và Token Versioning để quản lý đăng nhập và bảo mật cho người dùng.

## Kết Luận

Ứng dụng này mang lại giải pháp tiện lợi và hiệu quả cho các trung tâm dưỡng lão, giúp người nhà dễ dàng chăm sóc và theo dõi người thân, đồng thời hỗ trợ nhân viên quản lý công việc một cách dễ dàng và nhanh chóng.

