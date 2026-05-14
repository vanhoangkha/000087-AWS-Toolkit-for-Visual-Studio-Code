---
title: "Kết nối tài khoản AWS"
date: 2024-01-01
weight: 3
chapter: false
pre: "<b> 3. </b>"
---

#### Hướng Dẫn Kết Nối AWS Toolkit Cho Visual Studio Code Với Tài Khoản AWS

AWS Toolkit cho Visual Studio Code là một công cụ hỗ trợ đắc lực cho các nhà phát triển sử dụng dịch vụ của Amazon Web Services (AWS). Để sử dụng đầy đủ chức năng của Toolkit, bạn cần phải có một tài khoản AWS. Tuy nhiên, bạn vẫn có thể khám phá một số tính năng của Toolkit mà không cần kết nối tới tài khoản.

Nếu bạn đã từng thiết lập tài khoản AWS và xác thực qua các dịch vụ khác của AWS như AWS Command Line Interface, AWS Toolkit sẽ tự động phát hiện các thông tin đăng nhập của bạn.

#### Các Bước Chuẩn Bị

Dưới đây là ba bước chính để bạn có thể kết nối AWS Toolkit với tài khoản AWS của mình:

#### 1. Đăng ký tài khoản AWS

Bạn có thể đăng ký tài khoản AWS thông qua cổng đăng ký của AWS. Để biết thông tin chi tiết về cách thiết lập một tài khoản AWS mới, bạn có thể tham khảo trong mục Tổng quan của Hướng dẫn thiết lập AWS.

#### 2. Thiết lập xác thực

Có ba phương thức xác thực chính để kết nối với tài khoản AWS của bạn từ AWS Toolkit:
- Xác thực và kết nối với AWS IAM Identity Center
- Xác thực và kết nối với IAM Credentials
- Xác thực và kết nối với AWS Builder ID

#### 3. Xác thực với AWS từ Toolkit

Bạn có thể kết nối với tài khoản AWS của mình từ Toolkit bằng cách hoàn tất các thủ tục trong các mục tiếp theo của hướng dẫn này.

#### Mở Panel Đăng Nhập AWS Toolkit

#### Từ AWS Explorer

- Mở AWS Toolkit cho Visual Studio Code và mở rộng mục EXPLORER.
- Chọn biểu tượng ... để mở rộng menu More Actions...
- Chọn Connect to AWS để mở panel đăng nhập AWS Toolkit.

#### Sử dụng bảng lệnh của VS Code

- Mở bảng lệnh bằng cách nhấn Shift+Command+P (hoặc Ctrl+Shift+P trên Windows).
- Nhập AWS: Add a New Connection vào trường tìm kiếm.
- Chọn AWS: Add a New Connection để mở panel đăng nhập AWS Toolkit.

![Amazon Q](/images/00016.png?featherlight=false&width=90pc)

#### Kết Nối Với AWS Từ Toolkit

Để xác thực và kết nối với AWS sử dụng AWS IAM Identity Center, hoàn thành các bước sau:
- Trong panel đăng nhập AWS Toolkit, chọn tab Workforce và sau đó chọn nút Continue.
- Trong panel Sign in with IAM Identity Center, nhập Start URL cho tổ chức của bạn.
- Chọn AWS Region từ menu thả xuống.
- Chọn nút Continue và xác nhận bạn muốn mở website yêu cầu xác thực AWS trong trình duyệt mặc định của bạn.
- Làm theo hướng dẫn trên trình duyệt, bạn sẽ được thông báo khi quá trình xác thực hoàn tất.

Với các bước trên, bạn đã có thể bắt đầu làm việc với AWS Toolkit cho Visual Studio Code một cách hiệu quả.
