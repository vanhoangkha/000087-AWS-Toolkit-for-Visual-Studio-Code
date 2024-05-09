---
title: "AWS Explorer"
date: "`r Sys.Date()5"
weight: 1
chapter: false
pre: "<b>6.1</b>"
---

#### Sử dụng AWS Explorer trong Visual Studio Code

AWS Explorer cung cấp cho bạn một cái nhìn về một số dịch vụ AWS mà bạn có thể làm việc với khi sử dụng AWS Toolkit cho Visual Studio Code.

Phần này cung cấp thông tin về cách truy cập và sử dụng AWS Explorer trong VS Code. Nó giả định rằng bạn đã cài đặt và cấu hình Toolkit cho VS Code trên hệ thống của bạn.

Một số điểm quan trọng:

- Nếu toolkit được cài đặt và cấu hình đúng cách, bạn sẽ thấy các mục trong AWS Explorer. Để xem AWS Explorer, chọn biểu tượng AWS trong thanh hoạt động.

Ví dụ:

Điều này giúp xác định cần thiết cho quyền mạng AWS. Ví dụ, để xem các chức năng Lambda AWS trong tài khoản AWS của bạn, thông tin xác thực bạn đã cấu hình trong Xác thực và truy cập phải bao gồm ít nhất quyền đọc Lambda. Xem các chủ đề sau đây để biết thêm thông tin về các quyền mạng mà mỗi chức năng cần.

- Nếu bạn muốn tương tác với các dịch vụ AWS không ngay lập tức hiển thị trong AWS Explorer, bạn có thể đi đến Tài nguyên khác và chọn từ hàng trăm tài nguyên có thể được thêm vào giao diện.

![Amazon Q](/images/00019.png?featherlight=false&width=90pc)

Ví dụ, bạn có thể chọn AWS Toolkit: CodeArtifact:: Repository từ danh sách các loại tài nguyên có sẵn. Sau khi loại tài nguyên này được thêm vào Tài nguyên khác, bạn có thể mở rộng mục để xem danh sách các tài nguyên tạo ra các kho lưu trữ CodeArtifact khác nhau với các thuộc tính và tính năng riêng của chúng. Hơn nữa, bạn có thể mô tả các thuộc tính và tính năng của các tài nguyên trong các mẫu được định dạng JSON, có thể được lưu để tạo ra các tài nguyên mới trong Đám mây AWS.
