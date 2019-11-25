## MySQL Temporary Table

Trong MySQL, một **temporary table** là một kiểu bảng đặc biệt cho phép bạn chứa một tập kết quả tạm thời (tmporary result set), bạn có thể sử dụng nó nhiều lần trong một phiên.

Temporary table rất tiện dụng khi không thể hoặc rất khó để truy vấn dữ liệu mà yêu cầu chỉ sử dụng một lệnh **SELECT** với các mệnh đề **JOIN**. Trong trường hợp này, bạn có thể dùng temporary table để lưu trữ kết quả ngay lập tức và sử dụng truy vấn khác để xử lý nó.

Một temporary table có các tính năng đặc biệt sau:

  - Một temporary table được tạo bằng cách sử dụng lênh **CREATE TEMPORARY TABLE**. Lưu ý rằng từ khóa **TEMPORARY** được thêm vào giữa từ khóa **CREATE** và **TABLE**.
  - MySQL tự động xóa temporary table khi phiên đó kết thúc hoặc kết nối bị ngắt. Tất nhiên, bạn có thể dùng lệnh **DROP TABLE** để xóa hoàn toàn temporary table khi bạn không dùng nó nữa.
  - Một temporary table chỉ có thể truy cập bởi client tạo ra nó. Các client khác có thể tạ các temporary table cùng tên mà không gây ra lỗi bởi vì chỉ client tạo ra temporary table mới thấy nó. Tuy nhiên, trong cùng một phiên, 2 temporary table không thể dùng chung tên.
  - Một temporary table có thể có cùng tên với một bảng thông thường trong một cơ sở dữ liệu. Nếu bạn tạo một temporary table có tên là **Table_1** trùng tên với một bảng bình thường cũng có tên là **Table_1** trong một cơ sở dữ liệu thì bảng bình thường đó sẽ bị vô hiệu hóa. Tất cả truy vấn bạn gửi tới bảng **Table_1** sẽ truy vấn tới temporary table **Table_1**. Khi bạn bỏ temporary table **Table_1** thì bảng **Table_1** thật mới có thể tiếp tục truy nhập.

### Tạo một Temporary Table

Lệnh tạo một temporary table hoàn toàn giống với lệnh tạo một bảng thông thường mới ngoại trừ từ khóa TEMPORARY.

> CREATE TEMPORARY TABLE table_name (
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_1_definition,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_2_definition,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . . . ;
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; table_constraints
<br>);

Để tạo một temporary table có cấu trúc dựa trên một bạng đã có sẵn, sử dụng lệnh sau:

>CREATE TEMPORARY TABLE temp_table_name
<br> SELECT * FROM original_table
<br>LIMIT 0;

 
