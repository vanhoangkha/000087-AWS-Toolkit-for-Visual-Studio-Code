---
title: "Tạo AWS Builder ID"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b> 5.3 </b>"
---

#### Tạo AWS Builder ID

Khi đăng ký sử dụng các công cụ và dịch vụ của AWS với một AWS Builder ID, bạn sẽ tạo AWS Builder ID của riêng mình. Quá trình đăng ký bao gồm việc đăng ký với địa chỉ email, tên và mật khẩu.

#### Yêu Cầu Về Mật Khẩu

- Mật khẩu phải phân biệt chữ hoa và chữ thường.
- Mật khẩu phải có độ dài từ 8 đến 64 ký tự.
- Mật khẩu phải bao gồm ít nhất một ký tự từ mỗi danh mục sau:
  - Chữ cái thường (a-z)
  - Chữ cái hoa (A-Z)
  - Số (0-9)
  - Ký tự không phải chữ số và không phải chữ cái (~!@#$%^&*_-+=\`|(){}[]:;"’<>,.?/)
- Ba mật khẩu gần nhất không thể tái sử dụng.
- Mật khẩu không được sử dụng nếu đã bị tiết lộ trong một vụ rò rỉ dữ liệu của bên thứ ba.

*Lưu ý:* Các công cụ và dịch vụ sử dụng AWS Builder ID sẽ hướng dẫn bạn cách tạo và sử dụng AWS Builder ID khi cần thiết.

#### Cách Tạo AWS Builder ID

- Truy cập trang đăng ký của công cụ hoặc dịch vụ AWS mà bạn muốn truy cập, hoặc vào trang **AWS Builder ID profile**.

![Amazon Q](/images/0008.png?featherlight=false&width=90pc)

- Trên trang **Create AWS Builder ID**, nhập **Email Address** của bạn. Chúng tôi khuyên bạn nên sử dụng email cá nhân.
- Nhấn **Next**.
- Nhập **Name** của bạn, sau đó nhấn **Next**.

![Amazon Q](/images/00010.png?featherlight=false&width=90pc)

- Trên trang **Email Verification**, nhập mã xác minh được gửi đến địa chỉ email của bạn. Nhấn **Verify**. Tùy thuộc vào nhà cung cấp email của bạn, có thể mất vài phút để nhận được email. Kiểm tra trong thư mục spam và thư rác để tìm mã. Nếu bạn không nhận được email từ AWS sau năm phút, nhấn **Resend Code**.
- Sau khi chúng tôi xác minh email của bạn, trên trang **Choose a Password**, nhập **Password và Confirm Password** của bạn.
- Nếu xuất hiện Captcha như một biện pháp bảo mật bổ sung, nhập các ký tự bạn thấy.

![Amazon Q](/images/00011.png?featherlight=false&width=90pc)

- Nhấn **Create AWS Builder ID**.

#### Thiết Bị Đáng Tin Cậy (Trusted Devices)

Sau khi bạn chọn tùy chọn Thiết Bị Đáng Tin Cậy từ trang đăng nhập, chúng tôi coi tất cả các lần đăng nhập sau đó từ trình duyệt web trên thiết bị đó là được ủy quyền. Điều này có nghĩa là bạn sẽ không cần cung cấp mã MFA trên thiết bị đáng tin cậy đó. Tuy nhiên, nếu trình duyệt, cookie hoặc địa chỉ IP của bạn thay đổi, bạn có thể cần sử dụng mã MFA để xác minh thêm.

#### Xác thực và Kết nối Sử dụng AWS Builder ID

Trong phần giao diện người dùng **Sign in to Get Started**, chọn nút **Use for free with AWS Builder ID** và xác nhận bạn muốn tiếp tục đến trang yêu cầu xác thực AWS trên trình duyệt web mặc định của bạn.

![Amazon Q](/images/00016.png?featherlight=false&width=90pc)

Trên trình duyệt web mặc định của bạn, xác nhận rằng mã xác thực khớp với mã từ VS Code, sau đó chọn nút **Confirm and continue** để tiếp tục.

![Amazon Q](/images/00013.png?featherlight=false&width=90pc)

Tuân theo hướng dẫn trên trình duyệt web mặc định của bạn. Bạn sẽ nhận được thông báo khi quá trình xác thực hoàn tất, và bạn có thể đóng trình duyệt và quay lại VS Code.

![Amazon Q](/images/00014.png?featherlight=false&width=90pc)

![Amazon Q](/images/00015.png?featherlight=false&width=90pc)
