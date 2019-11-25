## MySQL Select Database.

Để chọn một cơ sở dữ liệu cụ thể nào đó để làm việc, ta dùng lệnh **USE**:

> USE database_name;

Với *database_name* là tên của cơ sở dữ liệu muốn chọn.

Để chọn một cơ sở dữ liệu ta có các bước sau:

1. Đăng nhập vào **MySQL** sử dụng một urser cụ thể (ví dụ **root**):
  >mysql -u root -p

  Lệnh trên xác định user **root** với cờ *-u* và sau đó là cờ *-p*.  MySQL sẽ yêu cầu nhập mật khẩu của user, nhập mật khẩu gõ **ENTER** để log in.

2. Sử dụng lệnh **USE** để chọn một cơ sở dữ liệu:

>USE database_name;
>Database changed

Nếu cơ sở dữ liệu ta chọn tồn tại thì MySQL sẽ thông báo **Database changed**.

Nếu cơ sở dữ liệu không tồn tại, MySQL sẽ thông báo lỗi.

Có thể xem tên của cơ sở dữ liệu hiện đang kết nối bằng hàm **database()**:
>select database();

Chúng ta có thể chọn cơ sở dữ liệu mình muốn làm việc ngay trong khi chúng ta đăng nhập:

>mysql -u root -D database_name -p
