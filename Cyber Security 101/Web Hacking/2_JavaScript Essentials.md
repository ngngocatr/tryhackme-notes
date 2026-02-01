# JavaScript Essentials
## 1. Introduction
JavaScript (JS) là một ngôn ngữ lập trình kịch bản phổ biến cho phép các nhà phát triển web thêm các tính năng tương tác vào các trang web chứa HTML và CSS (kiểu dáng). Sau khi các phần tử HTML được tạo, bạn có thể thêm các tính năng tương tác như xác thực, hành động khi nhấp chuột, hoạt ảnh, v.v., thông qua JS. Học ngôn ngữ này cũng quan trọng như học HTML và CSS. Các đoạn mã JS chủ yếu được sử dụng với HTML.

Phòng học này được thiết kế như một khóa học tổng quan giới thiệu về JavaScript, đặc biệt dành cho người mới bắt đầu với kinh nghiệm JavaScript hạn chế. Trọng tâm chính là giảng dạy các nguyên tắc cơ bản của JavaScript từ góc độ an ninh mạng và cách tin tặc lợi dụng các chức năng hợp pháp để đạt được mục đích xấu.

### Mục tiêu học tập

- Nắm vững kiến ​​thức cơ bản về JavaScript.
- Tích hợp JavaScript vào HTML
- Lạm dụng chức năng hội thoại
- Bỏ qua các câu lệnh điều khiển luồng
- Khám phá các tệp tin được thu nhỏ

## 2. Essential Concepts(_Khái niệm_)
### 1. Biến
Biến là các vùng chứa cho phép bạn lưu trữ các giá trị dữ liệu trong đó. Giống như bất kỳ ngôn ngữ nào khác, biến trong JavaScript cũng tương tự như các vùng chứa để lưu trữ dữ liệu. Khi bạn lưu trữ thứ gì đó trong một cái xô, bạn cũng cần phải gắn nhãn cho nó để có thể dễ dàng tham chiếu lại sau này. Tương tự, trong JavaScript, mỗi biến đều có một tên; khi chúng ta lưu trữ một giá trị nhất định trong một biến, chúng ta gán cho nó một tên để tham chiếu lại sau này.Có 3 cách để khai báo biến trong JavaScript: `var`, `let`, `const`. Trong khi `var` có phạm vi hàm, cả `let`, `const` đều có phạm vi khối, cho phép kiểm soát tốt hơn khả năng hiển thị của biến trong các khối mã cụ thể.

<img src="../../images/2026-02-01-21-43-13.png" style="display: block; margin: 0 auto;">

### 2. Các kiểu dữ liệu
Trong JavaScript, kiểu dữ liệu xác định loại giá trị mà một biến có thể chứa. Ví dụ bao gồm `string`(văn bản), `number`, `boolean`(đúng/sai), `null`, `undefined` và `object` (dành cho dữ liệu phức tạp hơn như mảng hoặc đối tượng).

### 3. Chức năng
Hàm là một khối mã được thiết kế để thực hiện một nhiệm vụ cụ thể. Bên trong một hàm, bạn nhóm các đoạn mã cần thực hiện cùng một nhiệm vụ. Ví dụ, bạn đang phát triển một ứng dụng web mà bạn cần in kết quả học sinh lên trang web. Trường hợp lý tưởng là tạo một hàm `PrintResult(rollNum)` nhận số báo danh của người dùng làm đối số.

Vì vậy, thay vì viết cùng một đoạn mã in cho tất cả học sinh, chúng ta sẽ sử dụng một hàm đơn giản để in kết quả.

### 4. Vòng lặp
Vòng lặp cho phép bạn chạy một khối mã nhiều lần miễn là điều kiện được thỏa mãn **true**. Các vòng lặp phổ biến trong JavaScript là `while`, `for` , `do...while`, được sử dụng để lặp lại các tác vụ, chẳng hạn như duyệt qua một danh sách các mục. Ví dụ, nếu chúng ta muốn in kết quả của 100 học sinh, chúng ta có thể gọi hàm `PrintResult(rollNum)` 100 lần bằng cách viết nó 100 lần, hoặc chúng ta có thể tạo một vòng lặp sẽ lặp qua từ 1 đến 100 và sẽ gọi hàm `PrintResult(rollNum)` như được hiển thị bên dưới.
<img src="../../images/2026-02-01-21-53-33.png" style="display: block; margin: 0 auto;">

## 3. JavaScript Overview(_Tổng quan_)
Trong bài tập này, chúng ta sẽ sử dụng JavaScript để tạo chương trình đầu tiên. JavaScript là một ngôn ngữ **thông dịch** , nghĩa là mã được thực thi trực tiếp trong trình duyệt mà không cần biên dịch trước. Dưới đây là một đoạn mã JavaScript mẫu minh họa các khái niệm chính, chẳng hạn như **định nghĩa biến** , **hiểu về kiểu dữ liệu** , **sử dụng câu lệnh điều khiển luồng** và viết các hàm đơn giản. Những khối xây dựng thiết yếu này giúp tạo ra các ứng dụng web năng động và tương tác hơn. Đừng lo lắng nếu nó trông có vẻ hơi mới mẻ - chúng ta sẽ thảo luận chi tiết từng khái niệm này sau
<img src="../../images/2026-02-01-21-56-08.png" style="display: block; margin: 0 auto;">

JavaScript chủ yếu được thực thi ở phía máy khách, điều này giúp dễ dàng kiểm tra và tương tác với HTML trực tiếp trong trình duyệt. Chúng ta sẽ sử dụng `Google Chrome Console` tính năng này để chạy chương trình JavaScript đầu tiên, cho phép chúng ta viết và thực thi mã JavaScript một cách dễ dàng mà không cần công cụ bổ sung. Hãy làm theo các bước sau để bắt đầu:
- Mở `Google Chrome` bằng cách nhấp vào biểu tượng `Google Chrome` trên màn hình Desktop của máy ảo.

<img src="../../images/2026-02-01-21-57-58.png" style="display: block; margin: 0 auto;">

- Sau khi mở Chrome, nhấn `Ctrl + Shift + I` để mở `Console` hoặc nhấp chuột phải vào bất kỳ đâu trên trang và chọn `Inspect`.

<img src="../../images/2026-02-01-21-58-33.png" style="display: block; margin: 0 auto;">

- Sau đó, nhấp vào `Console` tab. Bảng điều khiển này cho phép bạn chạy mã JS trực tiếp trong trình duyệt mà không cần cài đặt thêm phần mềm.

<img src="../../images/2026-02-01-21-59-03.png" style="display: block; margin: 0 auto;">

- Hãy cùng tạo một chương trình JavaScript đơn giản để cộng hai số và hiển thị kết quả. Dưới đây là đoạn mã:

<img src="../../images/2026-02-01-21-59-37.png" style="display: block; margin: 0 auto;">

- Trong đoạn mã trên, `x` và `y` là các biến lưu trữ các số. `x + y`  một biểu thức cộng hai số lại với nhau, trong khi `console.log`  là một hàm được sử dụng để in kết quả ra màn hình console.\
Sao chép đoạn mã trên và dán vào bảng điều khiển bằng cách nhấn phím `Ctrl + V`. Sau khi dán, nhấn phím `Enter`. Bạn sẽ thấy kết quả hiển thị như sau

<img src="../../images/2026-02-01-22-00-34.png" style="display: block; margin: 0 auto;">

## 4. Integrating JavaScript in HTML(_Tich hợp JS vào HTML_)
Nhiệm vụ này giả định bạn có hiểu biết cơ bản về HTML và cấu trúc của nó. Phần này sẽ khám phá cách tích hợp JavaScript vào HTML. Thông thường, JavaScript không được sử dụng để hiển thị nội dung; nó hoạt động cùng với HTML và CSS để tạo ra các trang web động và tương tác. Có hai cách chính để tích hợp JavaScript vào HTML: nội bộ và bên ngoài.

### 1. Internal JS
JavaScript nội tuyến (Internal JS) đề cập đến việc nhúng mã JavaScript trực tiếp vào bên trong tài liệu HTML. Phương pháp này được ưa chuộng cho người mới bắt đầu vì nó cho phép họ thấy cách mã tương tác với HTML. Mã được chèn giữa các thẻ `<script>`. Các thẻ này có thể được đặt bên trong `<head>`, thường được sử dụng cho các mã cần được tải trước khi nội dung trang được hiển thị, hoặc bên trong `<body>`, nơi mã có thể được sử dụng để tương tác với các phần tử khi chúng được tải trên trang web.

<img src="../../images/2026-02-01-22-06-12.png" style="display: block; margin: 0 auto;">

Trong tài liệu HTML này, chúng ta đang sử dụng JavaScript nội bộ, nghĩa là mã được đặt trực tiếp bên trong tệp HTML trong thẻ `<script>` . Đoạn mã thực hiện một nhiệm vụ đơn giản: cộng hai số (`x` và `y`) và sau đó hiển thị kết quả trên trang web. JavaScript tương tác với HTML bằng cách chọn một phần tử `<p>` với **id="result"**  và cập nhật nội dung của nó bằng cách sử dụng `document.getElementById("result").innerHTML <script>`. Đoạn mã JavaScript nội bộ này được thực thi khi trình duyệt tải tệp HTML.

### 2. External JS
JavaScript bên ngoài (**External JS**) là việc tạo và lưu trữ mã JavaScript trong một tệp riêng biệt có phần mở rộng `.js`. Phương pháp này giúp các nhà phát triển giữ cho tài liệu HTML sạch sẽ và có tổ chức. Tệp JavaScript bên ngoài có thể được lưu trữ trên cùng máy chủ web với tài liệu HTML hoặc được lưu trữ trên một máy chủ web bên ngoài, chẳng hạn như trên đám mây.

Chúng ta sẽ sử dụng ví dụ tương tự cho JavaScript bên ngoài nhưng tách mã JavaScript đó ra thành một tệp riêng.

Đầu tiên, hãy tạo một tệp mới có tên `script.js` và lưu nó vào thư mục Desktop với đoạn mã sau:

<img src="../../images/2026-02-01-22-09-00.png" style="display: block; margin: 0 auto;">

Tiếp theo, tạo một tệp mới có tên `external.html` và dán đoạn mã sau vào đó (lưu ý rằng mã HTML giống với ví dụ trước):

<img src="../../images/2026-02-01-22-09-37.png" style="display: block; margin: 0 auto;">

Bây giờ, hãy nhấp đúp vào tệp external.html và kiểm tra kết quả. Bạn có thấy sự khác biệt nào không? Không, kết quả vẫn giống như ví dụ trước.

<img src="../../images/2026-02-01-22-09-58.png" style="display: block; margin: 0 auto;">

Điều chúng tôi làm khác biệt là sử dụng thuộc tính `src` trong thẻ `<script>` để tải mã JavaScript từ một tệp bên ngoài. Khi trình duyệt tải trang, nó sẽ tìm `script.js` và tải nội dung của nó vào tài liệu HTML. Cách tiếp cận này cho phép chúng ta tách biệt mã JavaScript khỏi HTML, giúp mã được tổ chức tốt hơn và dễ bảo trì hơn, đặc biệt là khi làm việc với các dự án lớn.

### 3. Xác minh JavaScript Internal hoặc External
Khi kiểm thử bảo mật một ứng dụng web, điều quan trọng là phải kiểm tra xem trang web đó có sử dụng JavaScript nội bộ hay bên ngoài. Điều này có thể dễ dàng được xác minh bằng cách xem mã nguồn của trang. Để làm điều này, hãy mở trang `external_test.html` nằm trong `exercise` thư mục `Chrome`, nhấp chuột phải vào bất kỳ đâu trên trang và chọn `View Page Source`.

<img src="../../images/2026-02-01-22-13-44.png" style="display: block; margin: 0 auto;">

Thao tác này sẽ hiển thị mã HTML của trang đã được render. Bên trong mã nguồn, bất kỳ mã JavaScript nào được viết trực tiếp trên trang sẽ xuất hiện giữa các thẻ `<script>` mà không có thuộc tính `src`. Nếu bạn thấy một thẻ `<script>` có thuộc tính `src` , điều đó cho thấy trang đang tải mã JavaScript external từ một tệp riêng biệt.

<img src="../../images/2026-02-01-22-15-07.png" style="display: block; margin: 0 auto;">

