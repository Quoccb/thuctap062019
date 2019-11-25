### MySQL Sequence

Trong MySQL, một **sequence** là một list các số nguyên được tạo theo thứ tự tăng dần.
Nhiều ứng dụng cần **sequence** để tạo các số độc nhất chủ yếu cho việc xác thực.

Để tạo một sequence tự động trong MySQL, cần thiết lập **AUTO_INCREMENT** cho một cột, chúng thường là cột **primary key**.

Cần tuân thủ các quy định sau đây khi sử dụng thuộc tính **AUTO_INCREMENT**:

  - Mỗi bảng chỉ có duy nhất một cột **AUTO_INCREMENT** có kiểu dữ liệu thường là integer.
  - Cột **AUTO_INCREMENT** phải được lập chỉ mục, có nghĩa là nó có thể là chỉ số **PRIMARY KEY** hoặc **UNIQUE**
  - Cột **AUTO_INCREMENT** phải có quy chế **NOT NULL**. Khi dùng thuộc tính **AUTO_INCREMENT** cho một cột, MySQL sẽ tự dộng thêm **NOT NULL** vào cột.
