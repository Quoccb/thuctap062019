## MySQL ALTER TABLE

Lệnh **ALTER TABLE** có thể dùng để thêm, hiệu chỉnh, đổi tên, xóa một cột hoặc đổi tên một bảng.

### Thêm cột vào một bảng.

Lệnh **ALTER TABLE ADD** cho phép bạn thêm một hoặc nhiều cột vào một bảng.

  1. Thêm một cột vào một bảng.

  Để thêm một cột vào một bảng, dùng lệnh sau:

  > ALTER TABLE table_name
  <br> ADD
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; new_column_name column_definition
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [FIRST | AFTER column_name]

  Trong đó:

    - **table_name** : là tên của bảng mà bạn muốn thêm cột mới, được đặt sau từ khóa **ALTER TABLE**.
    - **new_column_name** : là tên của cột mới.
    - **column_definition** : xác định kiểu dữ liệu, kích thước tối đa, và các quy ước của cột mới.
    - **[FIRST | AFTER column_name]** xác định vị trí của cột mới trọng bảng. Bạn có thể thêm một cột vào sau một cột đã có (**AFTER column_name**) hoặc làm cột đầu tiên (**FIRST**). Nếu bỏ qua mệnh đề này, cột sẽ được thêm vào cuối bảng.


  2. Thêm nhiều cột vào một bảng.

  Để thêm nhiều cột vào một bảng, dùng lệnh sau:

  >ALTER TABLE table_name
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ADD new_column_name column_definition
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [FIRST | AFTER column_name],
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ADD new_column_name column_definition
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [FIRST | AFTER column_name],
  <br> . . . ;

### Chỉnh sửa cột.

1. Chỉnh sửa một cột.

>ALTER TABLE table_name
<br>MODIFY column_name column_definition
<br> [ FIRST | AFTER column_name];

2. Chỉnh sửa nhiều cột.

>ALTER TABLE table_name
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MODIFY column_name column_definition
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [ FIRST | AFTER column_name],
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MODIFY column_name column_definition
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [ FIRST | AFTER column_name],
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . . . ;

### Đổi tên cột.

>ALTER TABLE table_name
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; CHANGE COLUMN original_name new_name column_definition
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [FIRST | AFTER column_name];

### Bỏ một cột.

> ALTER TABLE table_name
<br>DROP COLUMN column_name;

### Đổi tên bảng.

>ALTER TABLE table_name
<br>RENAME TO new_table_name;
