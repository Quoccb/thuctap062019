### 1. Webserver là gì?
**Web server** hay còn gọi là máy chủ Web, nó là một chương trình sử dụng giao thức HTTP, để cung cấp các file để tạo thành các trang của website cho người dùng đáp ứng nhu cầu của họ, cuối cùng được phân phát đến thiết bị của user.

  <img src=https://dieuhau.com/wp-content/uploads/2016/11/cach-web-server-hoat-dong.jpg>

### 2. Nginx là gì?
  Nginx là một máy chủ proxy ngược mã nguồn mở (open source reverse proxy server) sử dụng phổ biến giao thức HTTP, HTTPS, SMTP, POP3 và IMAP , cũng như dùng làm cân bằng tải (load balancer), HTTP cache và máy chủ web (web server).

**Cài đặt nginx:**
> yum install nginx

### 3. Apache là gì?
Apache hay là chương trình máy chủ HTTP là một chương trình dành cho máy chủ đối thoại qua giao thức HTTP. Apache chạy trên các hệ điều hành tương tự như Unix, Microsoft Windows, Novell Netware và các hệ điều hành khác.

**Cài đặt Apache:**
>yum install httpd


### 4. Cấu hình Apache
 * **File cấu hình của Apache là:**

 > /etc/httpd/conf/httpd.conf

    * **ServerRoot:**  Là đường dẫn đến các file cấu hình, error và log. Default là /etc/httpd.
    * **ServerName** Là nơi khai báo tên của website
    * **DocumentRoot** Là nơi đặt các web documents. Default directory là: /var/www/html.
    * **ErrorLog** Chỉ ra vị trí file Log chứa tất cả các lỗi server. Mặc định là */etc/httpd/logs/error_log*. Lưu ý răng */etc/httpd/logs* là symbolic link tới */etc/httpd/* nên thực tế thì Log ở */var/log/httpd/error_log*.
    * **Listen** Chỉ ra **Port** là **Web Server** sẽ bắt gói tin. Mặc định là **Port 80** cho **non-secure web communications** và **Port 443** cho **ecure web communications**
    * **Virtual Host** Cho phép chạy nhiều Websites trên một máy tính



File cấu hình Secure Web Server là:
> /etc/httpd/conf.d/ssl.conf

Thiết lập SSL certificate:

| Command | Description |
|----|-------|
|openssl genrsa -des3 -out myca.key 4096| Create CA key|
|openssl req -new -x509 -days 365 -key myca.key -out myca.crt | Create CA ertificate |
|openssl genrsa -des3 -out server.key 4096 | Create server key |
| openssl req -new -key server.key -out server.csr | Create CSR |
| openssl x509 -req -days 365 -in server.csr -CA myca.crt -CAkey myca.key -set_serial 01 -out server.crt | Sign CSR |
