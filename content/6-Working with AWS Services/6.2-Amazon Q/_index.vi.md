---
title: "Amazon Q"
date: 2024-01-01
weight: 2
chapter: false
pre: "<b> 6.2 </b>"
---

#### Làm việc với Amazon Q từ Toolkit

Amazon Q là một toolkit trò chuyện ngôn ngữ tự nhiên dựa trên trí tuệ nhân tạo có khả năng đề xuất mã cho các tập tin khác nhau, tạo PRs để được phê duyệt theo nhóm và triển khai chúng trong các dự án của bạn. Để biết thông tin chi tiết về dịch vụ Amazon Q, xem Hướng dẫn người dùng Amazon Q.

#### Yêu cầu tiên quyết

Để bắt đầu làm việc với Amazon Q, xác thực và kết nối với AWS bằng cách sử dụng ID AWS Builder hoặc thông tin đăng nhập IAM AWS của bạn. Xem các kế hoạch và giá cả chi tiết cho Amazon Q tại Hướng dẫn giá của Amazon Q. Để biết thông tin chi tiết về việc kết nối tài khoản AWS của bạn với Toolkit, xem phần Xác thực cho Amazon Q + CodeWhisperer trong Hướng dẫn người dùng này.

#### Trò chuyện với Amazon Q

Bắt đầu một cuộc trò chuyện với Amazon Q bằng cách đặt câu hỏi trong Chat. Amazon Q có thể thảo luận về nhiều chủ đề bao gồm AWS, phát triển phần mềm, ngôn ngữ lập trình và nhiều hơn nữa. Bạn cũng có thể đặt câu hỏi cụ thể về dự án của bạn cho Amazon Q trong VS Code. Để biết thông tin chi tiết về Amazon Q Chat, bao gồm các chủ đề và câu hỏi mẫu, xem chủ đề Amazon Q Chat trong Hướng dẫn người dùng Amazon Q.

Dưới đây là các lệnh Chat nhanh của Amazon Q mà bạn có thể nhập trong cửa sổ chat.

- `/clear`: Xóa chat hiện tại bằng cách loại bỏ tất cả văn bản và ngữ cảnh đã lưu trước đó.
- `/dev`: Bắt đầu một cuộc trò chuyện về phát triển các tính năng Amazon Q và tạo một kế hoạch triển khai cho dự án của bạn.
- `/transform`: Bắt đầu một cuộc trò chuyện về Chuyển đổi Mã Amazon Q, hỗ trợ bạn chuyển đổi mã từ một phiên bản ngôn ngữ sang một phiên bản khác.
- `/help`: Hiển thị một danh sách các chủ đề trợ giúp và thông tin về Amazon Q.

Để bắt đầu một cuộc trò chuyện mới với Amazon Q hoặc truy cập một cuộc trò chuyện hiện có, làm theo một trong các thủ tục dưới đây.

#### Mở Amazon Q Chat từ thanh công cụ VS Code

Từ thanh công cụ VS Code, chọn biểu tượng Amazon Q (phiên bản xem trước) để mở cửa sổ Chat Amazon Q (phiên bản xem trước). Bắt đầu một cuộc trò chuyện mới bằng cách chọn biểu tượng +. Nhập câu hỏi hoặc lệnh của bạn vào trường văn bản "Đặt câu hỏi hoặc nhập '/'" để tiếp tục cuộc trò chuyện.

#### AWS Toolkit - Amazon Q, CodeWhisperer và nhiều hơn nữa

#### Phát triển tính năng với Amazon Q

Phát triển dự án của bạn bằng cách trò chuyện với Amazon Q về loại tính năng bạn muốn tạo. Giải thích các tính năng mong muốn trong cuộc trò chuyện và Amazon Q sẽ tạo ra một kế hoạch triển khai cho dự án mới hoặc hiện tại của bạn. Để biết thông tin chi tiết về việc phát triển tính năng với Amazon Q, xem chủ đề Phát triển tính năng với Amazon Q trong Hướng dẫn người dùng Amazon Q.

> Lưu ý: Phát triển tính năng Amazon Q chỉ có thể truy cập được với xác thực nhận dạng IAM. Xem kế hoạch và giá cả chi tiết của Amazon Q tại Hướng dẫn giá của Amazon Q.

Amazon Q không sửa đổi hoặc cập nhật mã cho đến khi bạn đã xem xét và phê duyệt thay đổi trong tệp diff. Để bắt đầu phát triển tính năng với Amazon Q, hoàn thành các bước sau:

- Từ dự án VS Code mới hoặc hiện có, mở Amazon Q Chat.
- Trong cửa sổ Amazon Q Chat, nhập `/dev`, sau đó nhấn enter để bắt đầu phát triển tính năng Amazon Q; trường văn bản Chat Amazon Q được cập nhật với lời nhắc "Mô tả ngắn gọn một nhiệm vụ hoặc vấn đề".
- Phản hồi với lời nhắc trong cửa sổ Chat Amazon Q, mô tả ngắn gọn tính năng bạn muốn phát triển, sau đó nhấn enter để bắt đầu tạo kế hoạch triển khai.
- Amazon Q phản hồi với một kế hoạch triển khai khi hoàn tất, và trường văn bản được cập nhật với lời nhắc.
- Nhập bất kỳ sửa đổi hoặc câu hỏi nào về kế hoạch triển khai vào trường văn bản.
- Khi hài lòng với kế hoạch, chọn Viết Mã từ cửa sổ chat để Amazon Q đề xuất mã cho dự án của bạn.

#### Tích hợp và khả năng trò chuyện trong môi trường phát triển tích hợp (IDEs)

Như chúng tôi đã đề cập, Amazon Q cũng có sẵn trong các IDE được hỗ trợ. Điều này cho phép bạn đặt câu hỏi và nhận sự trợ giúp trong IDE của bạn bằng cách trò chuyện với Amazon Q hoặc kích hoạt các hành động bằng cách nhập / vào hộp trò chuyện.

#### Phát triển tính năng năng lực

Một tính năng hấp dẫn khác mà Amazon Q cung cấp là hướng dẫn bạn tương tác từ ý tưởng đến việc xây dựng các tính năng mới trong IDE của bạn và Amazon CodeCatalyst. Bạn có thể chuyển từ một lời nhắc bằng ngôn ngữ tự nhiên thành các tính năng ứng dụng trong vài phút, với hướng dẫn tương tác từng bước và các quy ước tốt nhất, ngay từ IDE của bạn. Với một lời nhắc, Amazon Q sẽ cố gắng hiểu cấu trúc ứng dụng của bạn và phân tích cú pháp lời nhắc của bạn thành các bước triển khai logic và nguyên tử.

Để sử dụng tính năng này, bạn có thể bắt đầu bằng cách gọi một lệnh hành động /dev trong Amazon Q và mô tả nhiệm vụ mà bạn cần Amazon Q xử lý.

Sau đó, từ đây, bạn có thể xem xét, hợp tác và hướng dẫn Amazon Q trong cuộc trò chuyện về các khu vực cụ thể cần triển khai.

![Amazon Q](/images/00025.png?featherlight=false&width=90pc)

Các khả năng bổ sung để giúp bạn phát hành các tính năng nhanh hơn với các yêu cầu pull requests đầy đủ có sẵn nếu bạn đang sử dụng Amazon CodeCatalyst. Trong Amazon CodeCatalyst, bạn có thể chỉ định một vấn đề mới hoặc đã tồn tại cho Amazon Q, và nó sẽ xử lý một quy trình phát triển end-to-end cho bạn. Amazon Q sẽ xem xét mã hiện tại, đề xuất một phương pháp giải quyết, tìm kiếm phản hồi từ bạn về phương pháp, tạo mã sẵn sàng cho việc hợp nhất, và đăng một yêu cầu pull request để xem xét. Tất cả những gì bạn cần làm sau đó là xem xét các giải pháp được đề xuất từ Amazon Q.

Các bức ảnh sau đây hiển thị một yêu cầu pull được tạo bởi Amazon Q trong Amazon CodeCatalyst.

![Amazon Q](/images/00026.png?featherlight=false&width=90pc)

#### Nâng cấp ứng dụng với Amazon Q Code Transformation

Với Amazon Q, bạn có thể nâng cấp một ứng dụng toàn bộ chỉ trong vài giờ bằng cách bắt đầu một quy trình biến đổi mã hướng dẫn. Khả năng này, được gọi là Amazon Q Code Transformation, giúp đơn giản hóa việc duy trì, di chuyển và nâng cấp ứng dụng hiện có của bạn.

Để bắt đầu, hãy điều hướng đến phần CodeWhisperer và sau đó chọn Transform. Amazon Q Code Transformation tự động phân tích cơ sở mã hiện tại của bạn, tạo ra một kế hoạch biến đổi và hoàn thành các nhiệm vụ biến đổi chính được đề xuất bởi kế hoạch.

![Amazon Q](/images/00027.png?featherlight=false&width=90pc)

**Thêm thông tin về tính năng này:**

- Amazon Q Code Transformation hiện đã có sẵn trong bản xem trước ngày hôm nay trong AWS Toolkit cho IntelliJ IDEA và AWS Toolkit cho Visual Studio Code.
- Để sử dụng khả năng này, bạn cần phải có Amazon CodeWhisperer Professional tier trong quá trình xem trước.
- Trong quá trình xem trước, bạn có thể nâng cấp các ứng dụng Java 8 và 11 lên phiên bản 17, một phiên bản phát hành hỗ trợ dài hạn (LTS) của Java.

#### Tăng Tốc Phát Triển Phần Mềm với Amazon Q

Amazon Q mang lại một loạt các tính năng và công cụ giúp tăng tốc quá trình phát triển phần mềm, từ gợi ý mã nguồn đến quét bảo mật và biến đổi mã nguồn.

#### Gợi Ý Mã Nguồn Trực Tiếp

Gợi ý mã nguồn trực tiếp giúp bạn viết mã nhanh hơn bằng cách hiển thị gợi ý khi bạn đang gõ.

**Ví dụ về gợi ý mã nguồn trực tiếp:**

![Amazon Q](/images/0001.gif?featherlight=false&width=90pc)

Hỗ trợ hơn 15 ngôn ngữ bao gồm Python, TypeScript, Rust, Terraform, AWS CloudFormation, và nhiều hơn nữa.

#### Trò Chuyện

Tạo mã nguồn, giải thích mã nguồn và nhận câu trả lời cho các câu hỏi về phát triển phần mềm.

**Ví dụ về trò chuyện với Amazon Q:**

![Amazon Q](/images/0002.gif?featherlight=false&width=90pc)

#### Quét Bảo Mật

Phân tích và sửa các lỗ hổng bảo mật trong dự án của bạn.

**Ví dụ về sửa lỗi lỗ hổng bảo mật:**

![Amazon Q](/images/0003.gif?featherlight=false&width=90pc)

Hỗ trợ 10 ngôn ngữ bao gồm Python, TypeScript, C#, và nhiều hơn nữa.

#### Agent Cho Phát Triển Phần Mềm

Amazon Q có thể lập kế hoạch và triển khai chức năng mới trên nhiều tệp trong không gian làm việc của bạn.

Để mở menu hành động nhanh và chọn hành động "/dev", hãy gõ "/" trong trò chuyện.

![Amazon Q](/images/0004.gif?featherlight=false&width=90pc)

Lưu ý: Bản demo này đã được rút gọn, việc tạo kế hoạch và mã có thể mất vài phút.

#### Agent Cho Biến Đổi Mã Nguồn

Nâng cấp ứng dụng Java của bạn trong vài phút, không phải hàng tuần.

Để mở menu hành động nhanh và chọn hành động "/transform", hãy gõ "/" trong trò chuyện.

![Amazon Q](/images/0005.gif?featherlight=false&width=90pc)

Hiện hỗ trợ nâng cấp dự án Maven Java 8 hoặc 11 lên Java 17.

#### Bắt Đầu

- **Tính Năng Miễn Phí**: Tạo hoặc đăng nhập với ID Builder AWS (không cần tài khoản AWS!).
- **Tính Năng Pro**: Nếu tổ chức của bạn ở trong tầng phát triển Amazon Q Pro, đăng nhập với đăng nhập duy nhất.

Amazon Q không chỉ là một công cụ phát triển phần mềm, mà còn là một đối tác đáng tin cậy trong quá trình phát triển ứng dụng của bạn.



