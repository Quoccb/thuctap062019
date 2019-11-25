## MySQL Storage Engines.

MySQL cung cấp các công cụ lưu trữ khác nhau cho các bảng của nó:

  - MyISAM
  - InnoDB
  - MERGE
  - MEMORY (HEAP)
  - ARCHIVE
  - CSV
  - FEDERATED

Mỗi công cụ lưu trữ có những ưu điểm và nhước điểm riêng. Hiểu rõ tính năng của mỗi công cụ lưu trữ và chọn công cụ phù hợp nhất cho các table để tối đa hóa hiệu suất của cơ sở dữ liệu là điều rất quan trọng.

### MyISAM

Đây là kiểu Storage Engine mặc định khi tạo bảng và được dùng phổ biến nhất. MyISAM cho phép lập chỉ mục toàn cột (Full Text Index). Do đó, Storage Engine này cho tốc độ truy suất (Đọc và tìm kiếm) nhanh nhất trong các Storage Engine. Nhược điểm của MyISAM là hoạt động theo kiểu Table Level locking nên khi cập nhật (Thêm,xóa,sửa) 1 bản ghi nào đó trong cùng 1 table thì table đó sẽ bị khóa lại, không cho cập nhật (Thêm,xóa,sửa) cho đến khi thao tác cập nhật trước đó thực hiện xong. Ngoài ra, do thiết kế đơn giản và không kiểm tra ràng buộc dữ liệu nên loại Storage Engine này dễ bị hỏng chỉ mục và dễ bị Crash.

Trước MySQL Version 5.5, MyISAM là storage engine mặc định khi tạo một table mà không xác định rõ storage engine. Từ Version 5.5 trở đi, MySQL sử dụng InnoDB là storage engine mặc định.

### InnoDB

Đây là kiểu Storage Engine mới hơn MyISAM. Storage Engine này không hỗ trợ Full Text Index như MyISAM nhưng hỗ trợ quan hệ giữa các bảng (Khóa ngoại). Do đó, kiểu Storage này kiểm tra tính toàn vẹn dữ liệu và ràng buộc rất cao => Khó sảy ra tình trạng hỏng chỉ mục và Crash như MyISAM. Ngoài ra, kiểu Storage Engine này hoạt động theo cơ chế Row Level Locking nên khi cập nhật (Thêm,xóa,sửa) 1 bảng thì chỉ có bản ghi đang bị thao tác bị khóa mà thôi, các hoạt động khác trên table này vẫn diễn ra bình thường. Vì những tính chất trên, kiểu Storage Engine này thích hợp sử dụng cho Ngân hàng và các trang web có tần suất cập nhật dữ liệu cao như Mạng xã hội, diễn đàn.... Tuy nhiên, nó có nhược điểm là hoạt động tốn RAM hơn so với MyISAM.

### MEMORY

Đây là kiểu Storage Engine được lưu trữ dữ liệu trực tiếp lên RAM nên tốc độ truy xuất và cập nhật rất nhanh. Vì thế, nó được dùng làm các table chứa dữ liệu tạm, chứa các phiên làm việc của user... Khi khởi động lại dịch vụ MySQL thì dữ liệu trên bảng có Storage Engine là MEMORY sẽ mất hết dữ liệu. Chính vì thế nên khi các bạn khởi động lại mysqld trên VPS hay Server thì sẽ thấy số người online = 0 MEMORY sử dụng cơ chế table-level locking như MyISAM. Dung lượng của 1 bảng Storage Engine dạng MEMORY tối đa là bao nhiêu ? Nó phụ thuộc vào cấu hình thông số max_heap_table_size trong file my.cnf, mặc định 1 bảng kiểu MEMORY có dung lượng tối đa là 16MB. Nếu vượt quá bạn sẽ nhận được lỗi: Table xyz is full…

### MERGE

Một bảng MERGE là một bảng ảo kết hợp nhiều bảng MyISAM có cùng cấu trúc thành một bảng. Công cụ lưu trữ MERGE cũng được gọi là công cụ MRG_MyISAM. Bảng **MERGE** không có chỉ số riêng, thay vào đó nó sử dụng các chỉ số của các bảng thành phần.

Sử dụng MERGE table, bạn có thể tăng tốc hiệu suất khi **join** nhiều bảng. MySQL chỉ cho phép thực hiện các SELECT, DELETE, UPDATE và INSERT trên các bảng MERGE.

### ARCHIVE

Công cụ lưu trữ ARCHIVE cho phép lưu trữ một lượng lớn các bản ghi thành một định dạng nén để tiết kiệm không gian. Công cụ lưu trữ ARCHIVE nén một bản ghi khi nó được chèn và giải nến nó sử dụng thư viện *zlib*.

Các bảng ARCHIVE chỉ cho phép các lệnh  INSERT và SELECT. Các bảng ARCHIVE không hỗ trợ các chỉ mục 
