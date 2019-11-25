## MySQL UPDATE

Lệnh **UPDATE** chỉnh sửa dữ liệu hiện tại trong bảng. Bạn có thể dùng lệnh **UPDATE** để thay đổi giá trị trong một hoặc nhiều cột của một hàng hoặc nhiều hàng.

Ta có cú pháp:

>UPDATE [LOW_PRIORITY] [IGNORE] table_name
<br> SET
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_name1 = expr1,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; column_name2 = expr2,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . . .
<br> [WHERE
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; condition];

### MySQL UPDATE JOIN

>UPDATE T1, T2,
<br>[INNER JOIN | LEFT JOIN] T1 ON T1.C1 = T2.C1
<br>SET
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T1.C2 = T2.C2,
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; T2.C3 = expr
<br>WHERE condition

Trong đó:
  - Đầu tiên, chỉ định T1 (Bảng chính) và T2 (bảng mà bạn muốn T1 join vào) sau mệnh đề **UPDATE**.
Lưu ý rằng sau mệnh đề **UPDATE** phải chỉ định ít nhất một bảng.
Dữ liệu trong bảng không được chỉ định sau mệnh đề **UPDATE** sẽ không được update.
  - Sau đó, chỉ định kiểu **join** mà bạn muốn sử dụng có thể là **INNER JOIN** hoặc **LEFT JOIN**. Mệnh đề **JOIN** phải xuất hiện ngay sau mệnh đề **UPDATE**.
  - Tiếp theo, gán các giá trị mới cho các cột trong bảng T1 và/hoặc bảng T2 mà bạn muốn update.
  - Cuối cùng, chỉ định một điều kiện trong mệnh đề **WHERE** để giới hạn các hàng được update.
