# Firewall Fundamentals
## 1. What is purpose of a Firewall
Chúng ta thường thấy bảo vệ bên ngoài các trung tâm mua sắm, ngân hàng, nhà hàng và nhà ở. Những người bảo vệ này được bố trí ở lối vào các khu vực này để kiểm soát người ra vào. Mục đích của việc kiểm soát này là để đảm bảo không ai lẻn vào mà không được phép. Người bảo vệ đóng vai trò như một bức tường ngăn cách giữa khu vực của họ và người ra vào.

Hàng ngày, có rất nhiều lưu lượng truy cập đến và đi giữa các thiết bị kỹ thuật số của chúng ta và Internet mà chúng được kết nối. Điều gì sẽ xảy ra nếu ai đó lẻn vào giữa lượng truy cập khổng lồ này mà không bị phát hiện? Khi đó, chúng ta cũng cần một người bảo vệ cho các thiết bị kỹ thuật số của mình, người có thể kiểm tra dữ liệu đến và đi. Người bảo vệ này chính là tường lửa . Tường lửa được thiết kế để kiểm tra lưu lượng truy cập đến và đi của mạng hoặc thiết bị kỹ thuật số. Mục tiêu cũng giống như người bảo vệ ngồi bên ngoài một tòa nhà: không cho phép bất kỳ khách truy cập trái phép nào vào hệ thống hoặc mạng. Bạn hướng dẫn tường lửa bằng cách cung cấp cho nó các quy tắc để kiểm tra tất cả lưu lượng truy cập. Bất cứ thứ gì đến hoặc đi khỏi thiết bị hoặc mạng của bạn đều sẽ phải đối mặt với tường lửa trước tiên. Tường lửa sẽ cho phép hoặc từ chối lưu lượng truy cập đó dựa trên các quy tắc được duy trì của nó. Hầu hết các tường lửa hiện nay đều vượt xa việc lọc dựa trên quy tắc và cung cấp thêm các chức năng để bảo vệ thiết bị hoặc mạng của bạn khỏi thế giới bên ngoài. Chúng ta sẽ thảo luận về tất cả các tường lửa này và thực hiện các bài thực hành trong phòng thí nghiệm trên một vài loại. 

<img src="../../images/2026-02-21-20-51-37.png" style="display: block; margin: 0 auto;">

### Mục tiêu học tập
Sau khi hoàn thành việc thiết kế phòng, bạn sẽ có hiểu biết cơ bản về các lĩnh vực sau:
- Các loại tường lửa
- Các quy tắc tường lửa và các thành phần của nó
- Hướng dẫn sử dụng tường lửa tích hợp sẵn của Windows 
- Hướng dẫn sử dụng tường lửa tích hợp sẵn trên Linux 

## 2. Types of Firewall
Việc triển khai tường lửa trở nên phổ biến trong các mạng sau khi các tổ chức phát hiện ra khả năng lọc lưu lượng truy cập độc hại khỏi hệ thống và mạng của họ. Sau đó, nhiều loại tường lửa khác nhau đã được giới thiệu, mỗi loại phục vụ một mục đích riêng biệt. Điều quan trọng cần lưu ý là các loại tường lửa khác nhau hoạt động trên các lớp khác nhau của mô hình OSI. Tường lửa được phân loại thành nhiều loại. 

Hãy cùng xem xét một vài loại tường lửa phổ biến nhất và vai trò của chúng trong mô hình OSI.

<img src="../../images/2026-02-21-20-54-51.png" style="display: block; margin: 0 auto;">

### 1. Stateless Firewall
Loại tường lửa này hoạt động ở lớp 3 và lớp 4 của mô hình OSI và chỉ hoạt động bằng cách lọc dữ liệu dựa trên các quy tắc đã được xác định trước mà không ghi nhận trạng thái của các kết nối trước đó. Điều này có nghĩa là nó sẽ khớp mọi gói tin với các quy tắc bất kể gói tin đó có thuộc về một kết nối hợp lệ hay không. Nó không lưu giữ thông tin về trạng thái của các kết nối trước đó để đưa ra quyết định cho các gói tin trong tương lai. Do đó, các tường lửa này có thể xử lý các gói tin nhanh chóng. Tuy nhiên, chúng không thể áp dụng các chính sách phức tạp cho dữ liệu dựa trên mối quan hệ của nó với các kết nối trước đó. Giả sử tường lửa từ chối một vài gói tin từ một nguồn duy nhất dựa trên các quy tắc của nó. Lý tưởng nhất, nó nên loại bỏ tất cả các gói tin trong tương lai từ nguồn này vì các gói tin trước đó không tuân thủ các quy tắc của tường lửa . Tuy nhiên, tường lửa liên tục quên điều này, và các gói tin trong tương lai từ nguồn này sẽ được coi là mới và được khớp lại với các quy tắc của nó.

### 2. Stateful Inspection Firewall
Không giống như tường lửa không trạng thái, loại tường lửa này không chỉ lọc gói tin theo các quy tắc đã định trước. Nó còn theo dõi các kết nối trước đó và lưu trữ chúng trong bảng trạng thái. Điều này bổ sung thêm một lớp bảo mật bằng cách kiểm tra các gói tin dựa trên lịch sử kết nối của chúng. Tường lửa có trạng thái hoạt động ở lớp `3` và lớp `4` của mô hình OSI. Giả sử tường lửa chấp nhận một vài gói tin từ một địa chỉ nguồn dựa trên các quy tắc của nó. Trong trường hợp đó, nó sẽ ghi lại kết nối này trong bảng trạng thái của mình và cho phép tất cả các gói tin trong tương lai cho kết nối này được tự động chấp nhận mà không cần kiểm tra từng gói tin. Tương tự, tường lửa có trạng thái ghi lại các kết nối mà chúng từ chối một vài gói tin, và dựa trên thông tin này, chúng từ chối tất cả các gói tin tiếp theo đến từ cùng một nguồn.

### 3. Proxy Firewall
Vấn đề của các tường lửa trước đây là chúng không thể kiểm tra nội dung của gói dữ liệu. Tường lửa proxy , hay cổng ứng dụng, hoạt động như trung gian giữa mạng riêng và Internet và hoạt động ở lớp `7` của mô hình OSI. Chúng cũng kiểm tra nội dung của tất cả các gói dữ liệu. Các yêu cầu do người dùng trong mạng đưa ra được proxy này chuyển tiếp sau khi kiểm tra và che giấu chúng bằng địa chỉ IP của chính nó để cung cấp tính ẩn danh cho các địa chỉ IP nội bộ. Các chính sách lọc nội dung có thể được áp dụng cho các tường lửa này để cho phép/từ chối lưu lượng truy cập đến và đi dựa trên nội dung của chúng.

### 4. Next-Generation Firewall
Đây là loại tường lửa tiên tiến nhất , hoạt động từ lớp 3 đến lớp 7 của mô hình OSI, cung cấp khả năng kiểm tra gói tin chuyên sâu và các chức năng khác giúp tăng cường bảo mật cho lưu lượng mạng đến và đi. Nó có hệ thống ngăn chặn xâm nhập, chặn các hoạt động độc hại trong thời gian thực. Nó cung cấp phân tích dựa trên kinh nghiệm bằng cách phân tích các mẫu tấn công và chặn chúng ngay lập tức trước khi tiếp cận mạng. NGFW có khả năng giải mã SSL/ TLS , kiểm tra các gói tin sau khi giải mã và đối chiếu dữ liệu với nguồn cấp dữ liệu tình báo về mối đe dọa để đưa ra các quyết định hiệu quả.

Bảng dưới đây liệt kê các đặc điểm của từng tường lửa , giúp bạn lựa chọn tường lửa phù hợp nhất cho các trường hợp sử dụng khác nhau.

<img src="../../images/2026-02-21-21-09-32.png" style="display: block; margin: 0 auto;">

