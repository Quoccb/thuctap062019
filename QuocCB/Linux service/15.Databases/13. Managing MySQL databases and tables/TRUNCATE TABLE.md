## MySQL TRUNCATE TABLE

Lệnh **TRUNCATE TABLE** cho phép bạn xóa tất cả dữ liệu trong một bảng.

Theo logic, **TRUNCATE TABLE** giống lệnh **DELETE** mà không sử dụng mệnh đề WHERE (xóa tất cả các hàng trong một bảng).

Tuy nhiê, Lệnh **TRUNCATE TABLE** hiệu quả hơn lệnh **DELETE** bởi vì nó loại bỏ và lập lại bảng thay vì xóa từng dòng một.

>TRUNCATE [TABLE] table_name;

Từ khóa **TABLE** là tùy chọn. Tuy nhiên, nên sử dụng từ khóa **TABLE** để phân biệt giữa lệnh **TRUNCATE TABLE** và hàm **TRUNCATE()**.

Nếu có bất kỳ **FOREIGN KEY** nào từ các bảng khác tham chiếu bảng mà bạn đang truncate thì lệnh **TRUNCATE TABLE** sẽ lỗi.

Lệnh **TRUNCATE TABLE** sẽ đặt lại giá trị ở cột **AUTO_INCREMENT** thành giá trị ban đầu nếu bảng đó có cột **AUTO_INCREMENT**.
