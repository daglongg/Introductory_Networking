# OSI - Open Systems Interconnection - Hệ thống kết nối mở

Đây là một mô hình tham chiếu xác định các tiêu chuẩn cho các giao thức truyền thống cũng như các chức năng của từng lớp. OSI được Tổ chức Tiêu chuẩn hóa Quốc tế phát triền và có kiến trúc 7 lớp. Mỗi lớp sẽ có các giao thức khác nhau.
Nhưng trong thực tế người ta hay sử dụng mô hình TCP/IP vì tính nhỏ gọn.

Mô hình OSI bao gồm 7 lớp:
*  `Application layer (Tầng ứng dụng)`: Lớp này cung cấp một số cách để thao tác dữ liệu (thông tin) thực sự cho phép bất kỳ loại người dùng nào truy cập mạng một cách dễ dàng. Lớp này cũng đưa ra yêu cầu đến lớp dưới cùng của nó, đó là lớp trình bày để nhận các loại thông tin khác nhau từ nó.
    * Ví dụ như: E-mail, chuyển tệp, phân phối kết quả cho người dùng, dịch vụ thư mục, tài nguyên mạng, v.v.
* `Presentation` (Tầng trình bày): Tầng này sử lý cú pháp, hoặc chuyển từ dữ liệu từ dạng này qua dạng khác. 
   * Ví dụ; Bạn đang thực hiện 1 việc gì đó qua mạng, dữ liệu sẽ được mã hóa và chuyển đi. Lớp này cũng sẽ đảm bảo dữ liệu được gửi theo cách mà người nhận sẽ hiểu được thông tin và sử dụng thông tin 1 cách hiệu quả.
* `Session` (Tầng phiên): Bộ điều khiển thoại mạng, thiết lập duy trì nhiều loại kết nối.
   * Ví dụ: Nếu như có bị ngắt kết nối thì tầng này sẽ chịu trách nhiệm kết nối lại, xác thực nếu xảy ra gián đoạn.
* `Transport`(Tầng vận chuyển): Tầng này chịu trách nhiệm điều phối, truyền dữ liệu cần gửi. Đảm bào dữ liệu được toàn vẹn dữ liệu.
   * Ví dụ: 2 giao thức phổ biến ở tầng này là TCP và UDP. TCP ưu tiên chất lượng hơn tốc độ. Còn UDP ưu tiên tốc độ hơn chất lượng. Nếu để ý kĩ thì ta sẽ thấy UDP thường được ứng dụng trong phát trực tiếp còn TCP được áp dụng trong khi ta upload file lên web.
* `Network` (Tầng mạng): Tầng này sẽ sử lý định tuyến dữ liệu, mỗi khung dữ liệu sẽ được kiếm tra để kết luận gói dữ liệu sẽ cần được đi tới điểm đích nào. Lớp này cũng sẽ quản lý ánh xạ giữa các địa chỉ IP được thực hiện thông qua hình thức phân giải địa chỉ IP ARP - Address Resolution Protocol.
* `Data Link`(Tầng Liên kết dữ liệu): Đây có thể là tầng phức tạp nhất, vai trò chính của nó là đảm bảo truyền tải thông tin không có lỗi. DLL cũng chịu trách nhiệm mã hóa, giải mã và tổ chức dữ liệu đi và đến. Lớp liên kết dữ liệu  được chia thành hai lớp con như sau
   * LLC: Logical Link Control: Lớp con này của lớp liên kết dữ liệu xử lý việc ghép kênh, luồng dữ liệu giữa các ứng dụng và các dịch vụ khác, đồng thời LLC cũng chịu trách nhiệm cung cấp các thông báo lỗi và xác nhận
   * MAC: Media Access Control: Lớp con MAC quản lý sự tương tác của thiết bị, chịu trách nhiệm đánh địa chỉ các khung và cũng kiểm soát quyền truy cập phương tiện vật lý. Lớp liên kết dữ liệu nhận thông tin dưới dạng các gói từ lớp Mạng, nó chia các gói thành các khung và gửi các khung đó từng bit đến lớp vật lý bên dưới.
* `Physical`(Tầng vật lý): Lớp vật lý nằm ngay dưới phần cứng của máy tính. Đây là nơi các xung điện tạo nên việc truyền dữ liệu qua mạng được gửi và nhận. Công việc của lớp vật lý là chuyển đổi dữ liệu nhị phân của quá trình truyền thành tín hiệu và truyền chúng qua mạng, cũng như nhận tín hiệu đến và chuyển đổi chúng trở lại thành dữ liệu nhị phân.

* 

