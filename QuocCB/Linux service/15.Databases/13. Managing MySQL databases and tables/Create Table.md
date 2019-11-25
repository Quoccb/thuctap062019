### MySQL CREATE TABLE syntax

Lệnh **CREAT TABLE** cho phép bạn tạo một bảng mới trong cơ sở dữ liệu.

>CREATE TABLE [IF NOT EXISTS] table_name(
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_1_definition,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_2_definition,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . . .,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; table_constraints
<br>) ENGINE=storage_engine;

Trong lệnh trên, đầu tiên bạn chỉ ra tên của bảng mà bạn muốn tạo sau từ khóa **CREATE TABLE**. Tên bảng đó phải là duy nhất trong một cơ sở dữ liệu. **IF NOT EXISTS** là tùy chọn. Nó giúp bạn kiểm tra xem bảng mà bạn tạo đã có trong cơ sở dữ liệu hay chưa. Nếu có rồi thì MySQL sẽ bỏ qua toàn bộ câu lệnh và sẽ không tạo bảng nào cả.

Sau đó bạn đưa ra một danh sách các cột của bảng trong phần **column_list**, các cột được phân cách bởi dấu phẩy.

Tiếp theo, bạn có thể tùy chọn chỉ ra công cụ lưu trữ cho bảng trong mệnh đề ENGINE. Bạn có thể sử dụng bất kỳ công cụ lưu trữ nào như InnoDB hay MyISAM. Nếu bạn không khai báo rõ một công cụ lưu trữ, MySQL sẽ mặc định sử dụng InnoDB.


Cú pháp khi xác định một cột:

>column_name data_type(length) [NOT NULL] [DEFAULT value] [AUTO_INCREMENT] column_constraint;

  - **column_name** chỉ ra tên của cột. Mỗi cột có một kiểu dữ liệu riêng và kích thước tùy chọn. Ví dụ: VARCHAR(255).
  - **NOT NULL** đảm bảo cột sẽ không chứa giá trị **NULL**. Bên cạnh quy ước **NOT NULL**, một cột có thể có thêm các quy ước tùy chọn khác như **CHECK**, **UNIQUE**.
  - **DEFAULT** chỉ ra giá trị mặc định cho cột.
  - **AUTO_INCREMENT** cho biết giá trị của cột được tự động tăng lên một đơn vị mỗi khi một hàng mới được chèn vào bảng. Mỗi bảng có tối đa 1 cột **AUTO_INCREMENT**.

Sau danh sách cột, bạn có thể xác định các quy ước của bảng như **UNIQUE**, **CHECK**, **PRIMARY KEY** và **FOREIGN KEY**.

> PRIMARY KEY (column1,column2,...)
