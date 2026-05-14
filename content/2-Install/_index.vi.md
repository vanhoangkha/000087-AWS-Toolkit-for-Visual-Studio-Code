---
title: "AWS Toolkit Cho Visual Studio Code"
date: 2024-01-01
weight: 2
chapter: false
pre: "<b> 2. </b>"
---

#### Bắt Đầu Sử Dụng AWS Toolkit Cho Visual Studio Code Trên VS Code

Để bắt đầu sử dụng AWS Toolkit cho Visual Studio Code từ VS Code, bạn cần đáp ứng các điều kiện sau:

- **Hệ điều hành**: VS Code yêu cầu một trong các hệ điều hành Windows, macOS hoặc Linux.
- **Phiên bản VS Code**: AWS Toolkit cho Visual Studio Code yêu cầu bạn làm việc từ phiên bản VS Code 1.73.0 trở lên.

Để biết thêm thông tin về VS Code hoặc tải xuống phiên bản mới nhất của VS Code, hãy truy cập [trang tải xuống VS Code](https://code.visualstudio.com/Download).

#### Tải và Cài Đặt AWS Toolkit Cho Visual Studio Code

Bạn có thể tải xuống, cài đặt và thiết lập AWS Toolkit cho Visual Studio Code thông qua VS Code Marketplace trong môi trường IDE của bạn. Hoặc, bạn có thể tải xuống các tệp cài đặt AWS Toolkit cho Visual Studio Code bằng cách điều hướng đến VS Code Marketplace từ trình duyệt web của bạn.

![Amazon Q](/images/0006.png?featherlight=false&width=90pc)

#### Cài Đặt AWS Toolkit Từ VS Code IDE Marketplace

1. Mở tiện ích mở rộng AWS Toolkit cho Visual Studio Code trong IDE VS Code của bạn với liên kết sau: [Mở VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-toolkit-vscode).
   
   > **Lưu Ý**: Nếu VS Code chưa đang chạy trên máy tính của bạn, quá trình này có thể mất một vài giây trong khi VS Code đang tải.

2. Từ tiện ích mở rộng AWS Toolkit trong VS Code Marketplace, chọn **Install** để bắt đầu quá trình cài đặt.

3. Khi được nhắc, chọn khởi động lại VS Code để hoàn tất quá trình cài đặt.

#### Điều Kiện Tiên Quyết Tùy Chọn

Trước khi bạn có thể sử dụng một số tính năng của AWS Toolkit cho Visual Studio Code, bạn cần có những thứ sau:

- **Tài khoản Amazon Web Services (AWS)**: Một tài khoản AWS không phải là yêu cầu để sử dụng AWS Toolkit cho Visual Studio Code, nhưng chức năng sẽ bị hạn chế đáng kể nếu không có nó. Để lấy một tài khoản AWS, hãy truy cập [trang chủ AWS](https://aws.amazon.com/), chọn **Create an AWS Account**, hoặc **Complete Sign Up** (nếu bạn đã truy cập trang này trước đó).

- **Phát Triển Mã – SDK phù hợp với ngôn ngữ bạn muốn sử dụng**. Bạn có thể tải xuống từ các liên kết sau, hoặc sử dụng trình quản lý gói yêu thích của bạn:
  - [.NET SDK](https://dotnet.microsoft.com/download)
  - [Node.js SDK](https://nodejs.org/en/download)
  - [Python SDK](https://www.python.org/downloads)
  - [Java SDK](https://aws.amazon.com/corretto/)
  - [Go SDK](https://golang.org/doc/install)

- **AWS SAM CLI** – Đây là một công cụ CLI của AWS giúp bạn phát triển, kiểm thử và phân tích các ứng dụng không máy chủ của mình một cách địa phương. Điều này không bắt buộc cho việc cài đặt toolkit. Tuy nhiên, chúng tôi khuyên bạn nên cài đặt nó (và Docker, được mô tả sau) vì nó là yêu cầu cho bất kỳ chức năng nào của Mô hình Ứng dụng Không Máy chủ AWS (AWS SAM), chẳng hạn như tạo một ứng dụng không máy chủ mới (local).
