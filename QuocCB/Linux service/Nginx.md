### I. Nginx là gì?
  Nginx là một máy chủ proxy ngược mã nguồn mở (open source reverse proxy server) sử dụng phổ biến giao thức HTTP, HTTPS, SMTP, POP3 và IMAP , cũng như dùng làm cân bằng tải (load balancer), HTTP cache và máy chủ web (web server).

### II. Kiến trúc của Nginx
  * Khi được khởi chạy service, nginx khởi tạo một tiến trình chủ và cũng là tiến trình duy nhất tồn tại trong bộ nớ ***Master Process***. Tiến trình này không chịu trách nhiệm tự xử lý bất kỳ request nào từ phía client mà thay vào đó nó sinh ra các tiến trình con gọi là Worker Process để xử lý các request này.
  <img src=https://viblo.asia/uploads/cfcdd863-8ade-4527-9149-2a89610467f2.jpg>

### III. Cấu hình http trong nginx
#### 1. Giới thiệu module Http trong Nginx
  - Module HTTP Core là thành phần chứa tất cả các khối, chỉ thị và các biến cơ bản của máy chủ HTTP.
  Mặc định module này được cài đặt trong khi biên dịch, nhưng không được bật lên khi Nginx chạy, việc sử dụng module này là không bắt buộc.

    **Trong module này có 3 khối chỉ thị chính**
    - **http:** Được khai báo ở phần đầu của tập tin cấu hình.
    Nó cho phép chúng ta định nghĩa các chỉ thị và các khối từ tất cả các module liên quan đến khía cạnh HTTP của Nginx. Khối chỉ thị này có thể được khai báo nhiều lần trong tập tin cấu hình, và các giá trị chỉ thị được chèn trong khối http sau sẽ ghi đè lên các chỉ thị nằm trong khối http trước đó
    - **server:** Khối này cho phép chúng ta khai báo 1 website. Nói cách khác, 1 website cụ thể (được nhận diện bởi 1 hoặc nhiều hostname) được thừa nhận bởi Nginx và nhận cấu hình của chính nó. Khối này chỉ có thể được dùng bên trong khối http.
    - **location:** Khối này cho phép chúng ta định nghĩa 1 nhóm các thiết lập được áp dụng cho 1 vị trí cụ thể trên website (Thể hiện qua URL của website đó).
    Khối location có thể được dùng bên trong 1 khối server hoặc nằm chồng bên trong 1 khối location khác.
    
