## DELETE

Để xóa dữ liệu từ một bảng, sử dụng lệnh **DELETE**.

>DELETE FROM table_name
<br> WHERE condition;

Câu lệnh trên được tiến hành như sau:

  - Đầu tiên, xác định bảng mà mình muốn xóa dữ liệu trong đó.
  - Sau đó, sử dụng một điều kiện trong mệnh đề **WHERE** để xác định những hàng cần xóa. Hàng nào thỏa mãn điều kiện thì sẽ bị xóa.

Lưu ý rằng mệnh đề **WHERE** là tùy chọn. Nếu bỏ qua mệnh đề **WHERE**, lệnh **DELETE** sẽ xóa tất cả các hàng trong bảng.

Không chỉ xóa dữ liệu trong bảng, lệnh **DELETE** còn trả về số hàng đã bị xóa.

Để xóa dữ liệu từ nhiều bảng bằng một câu lệnh **DELETE** duy nhất thì cần sử dụng lệnh **DELETE JOIN**.

Để xóa tất cả các hàng trong một bảng mà không quan tâm đến có bao nhiêu hàng bị xóa thì nên sử dụng lệnh **TRUNCATE TABLE** để đạt hiệu suất tốt hơn.

Với một bảng có ràng buộc **foreign key**, khi xóa các hàng từ bảng mẹ thì các hàng ở bảng con cũng tự động bị xóa bằng việc sử dụng tùy chọn **ON DELETE CASCADE**.

### DELETE JOIN

Như đã nói ở trên, đẻ xóa các hàng từ nhiều bảng ta sử dụng **DELETE JOIN**.

Chúng ta có thể sử dụng **INNER JOIN** hoặc **LEFT JOIN** trong lệnh **DELETE**.

1. **INNER JOIN**:

MySQL cho phép bạn sử dụng mệnh đề **INNER JOIN** trong lệnh **DELETE** để xóa các hàng từ một bảng và các hàng ở bảng khác match với các hàng đó.

>DELETE T1, T2
<br> FROM T1
<br> INNER JOIN T2 ON T1.key = T2.key
<br> WHERE condition;

Trong đó:
  - T1 và T2 là hai bảng chứa các hàng cần xóa.
  - T1.key = T2.key chỉ ra điều kiện mà các hàng giữa T1 và T2 nếu match nhau thì sẽ bị xóa.
  - **condition** trong mệnh đề **WHERE** là điều kiện để xác định các hàng trong T1 và T2 sẽ bị xóa.

2. **LEFT JOIN**

Chúng ta thường sử dụng **LEFT JOIN** trong câu lệnh **SELECT** để tìm các hàng trong bảng bên trái mà có thể có hoặc không có các hàng match với bảng bên phải.

Chúng ta cũng có thể dùng **LEFT JOIN** trong lệnh **DELETE** để xóa các hàng trong bảng bên phải mà không match với hàng nào ở bảng bên phải.

> DELETE T1
<br> FROM T1
<br> LEFT JOIN T2
<br> ON T1.key = T2.key
<br>WHERE T2.key IS NULL;

Lưu ý rằng chỉ để T1 sau từ khóa **DELETE** chứ không để cả **T1** và **T2** như **INNER JOIN**.

 
