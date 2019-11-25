### Creating databases

Trước khi làm việc với dữ liệu, bạn cần tạo một cơ sở dữ liệu.
Một cơ sở dữ liệu là một container của dữ liệu. Nó chứa contact, vendor, customer hay bất cứ loại dữ liệu nào mà bạn có thể biết.

Trong MySQL, một cơ sở dữ liệu là một tập hợp những đối tượng mà được sử dụng để chứa và xử lý dữ liệu như table, database views, trigger, và stored procedure.

Để tạo một cơ sở dữ liệu trong MySQL, sử dụng lệnh **CREATE DATABASE** như sau:

>CREATE DATABASE [IF NOT EXISTS] database_name;

Cùng xem xét câu lệnh trên chi tiết hơn:

   - Ngay sau lệnh **CREATE DATABASE** là tên cơ sở dữ liệu mà bạn muốn tạo. Tên cơ sở dữ liệu nên có ý nghĩa và có tính mô tả.
   - **IF NOT EXISTS** là một mệnh đề tùy chọn của câu lệnh. Mệnh đề **IF NOT EXISTS** giúp bạn tránh khỏi lỗi tạo một bảng mới mà nó đã tồn tại trong server cơ sở dữ liệu rồi. Bạn không thể có 2 cơ sở dữ liệu cùng tên trong một server cơ sở dữ liệu MySQL.


### Displaying Databases

Lệnh **SHOW DATABASES** sẽ liệt kê tất cả các cơ sở dữ liệu trong MySQL database server. bạn có thể dùng **SHOW DATABASES** để kiểm tra cơ sở dữ liệu mà bạn đã tạo hoặc để xem tất cả các cơ sở dữ liệu trên database server trước khi bạn tạo một cơ sở dữ liệu mới.

>SHOW DATABASES;

### Removing Databases

Xóa cơ sở dữ liệu có nghĩa là xóa vĩnh viễn tất cả các bảng trong cơ sở dữ liệu và cả chính cơ sở dữ liệu.

Để xóa một cơ sở dữ liệu, bạn dùng lệnh **DROP DATABASE** như sau:

>DROP DATABASE [IF EXISTS] database_name;

Sau mệnh đề **DROP DATABASE** là tên cơ sở dữ liệu mà bạn muốn xóa. Cũng giống như **CREATE DATABASE**, **IF EXISTS** là một tùy chọn của lệnh để tránh việc xóa một cơ sở dữ liệu mà nó không tồn tại trong database server.
