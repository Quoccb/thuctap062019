## MySQL Generated Columns

>column_name data_type [GENERATED ALWAYS] AS (experession)
<br>[VIRTUAL | STORED] [UNIQUE [KEY]]

Câu lệnh được xử lý theo các bước sau:

  1. Xác định tên cột (column_name) và kiểu dữ liệu (data_type) của nó.
  2. Thêm mệnh đề **GENERATED ALWAYS** để cho biết cột này một *generated column**.
  3. Chỉ ra kiểu của *generated column* bằng bằng tùy chọn tương ứng: **VIRTUAL** hoặc **STORED**. Mặc định, MySQL dùng **VIRTUAL** nếu bạn không xác định chính xác kiểu *generated column**.
  4. Chỉ ra *experession* trong dấu ngoặc đơn sau từ khóa **AS**. 
