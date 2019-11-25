

### MySQL INSERT

Câu lệnh **INSERT** cho phép chèn một hoặc nhiều hàng vào một bảng.

>INSERT INTO table(c1,c2,...)
<br>VALUES (v1,v2,...);

Trong đó **INSERT INTO** và **VALUES** là các **key word**, **table** là tên bảng, **(c1,c2,...)** là các cột và **(v1,v2,...)** là các giá trị tương ứng của các cột.

Số lượng các cột và các giá trị phải bằng nhau. Bên cạnh đó, vị trí của các cột phải tương ứng với vị trí của các giá trị.

Để chèn nhiều dòng vào một bảng bằng câu lệnh **INSERT**, sử dụng cú pháp sau:

>INSERT INTO table(c1,c2,...)
<br>VALUES
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (v11,v12,...),
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (v21,v22,...),
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . . .
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (vn1,vn2,...);


Theo lý thuyết, có thể chèn bao nhiêu hàng tùy thích trong một câu lệnh **INSERT**.
Tuy nhiên, khi MySQL server  nhận lệnh **INSERT** với tổng dung lượng lớn hơn **max_allowed_packet** thì sẽ xảy ra lỗi **packet too large** và kết thúc kết nối.

Dùng lệnh sau để hiện giá trị của biến **max_allowed_packet**:

>SHOW VARIABLES LIKE 'max_allowed_packet';

Giá trị của biến được biểu diễn theo đại lượng **bytes**.

Bên cạnh việc sử dụng các giá trị của hàng trong mệnh đền **VALUES**, còn có thể sử dụng kết quả của câu lệnh **SELECT** như là nguồn dữ liệu cho câu lệnh **INSERT**.

Ta có cú pháp:

>INSERT INTO table_name(column_list)
<br>SELECT
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; select_list
<br>FROM
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; another_table
<br>WHERE
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; condition;

Trong cú pháp trên, thay vì sử dụng mệnh đề **VALUES**, ta có thể sử dụng câu lệnh **SELECT**. Lệnh **SELECT** có thể truy xuất dữ liệu từ một hoặc nhiều bảng.

Lệnh **INSERT INTO SELECT** rất hữu dụng khi muốn copy dữ liệu từ các bảng khác sang một bảng hoặc tổng hợp dữ liệu từ nhiều bảng sang một bảng.

### INSERT IGNORE

Khi sử dụng lệnh **INSERT** để thêm nhiều hàng vào một bảng và nếu xảy ra lỗi trong quá trình xử lý, MySQL sẽ dừng lệnh và trả về lỗi. Kết quả là không có hàng nào được chèn vào trong bảng.

Tuy nhiên, nếu ban sử dụng lệnh **INSERT IGNORE**, các hàng có dữ liệu không hợp lệ gây ra lỗi sẽ bị bỏ qua và các hàng hợp lệ sẽ được chèn vào bảng.

Ta có cú pháp:

>INSERT IGNORE INTO table(column_list)
<br>VALUES
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (value_list),
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (value_list),
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  . . .
