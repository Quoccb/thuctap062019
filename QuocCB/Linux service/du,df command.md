**du** và **df** là hai lệnh phổ biến được dùng trong linux để tính toán kích thước tập tin, thư mục và không gian đĩa.
- **du** - Disk usage: Báo cáo lượng không gian trên đĩa đã được dùng bởi tập tin hay thư mục.
- **df** - Disk Free: Báo cáo lượng không gian lưu trữ còn trống trên đĩa.

### Lệnh du

- *du*: in ra không gian đĩa của thư mục hiện tại.
- *du file*: in ra kích thước file.
- *du --apparent-size file*: in ra kích thước thật của tập tin thay cho kích thước trên đĩa <br>
Đơn vị mặc định của du là 1024 byte. Chúng ta có thể thay đổi giá trị này bằng cách sử dụng tùy chọn -B hay –block-size như sau:
 <br> - **du -B SIZE FILE**
 <br> - **du --block-size=SIZE FILE**

Khi sử dụng du với thư mục, **du** chỉ xuất ra kích thước của thư mục này và các thư mục con bên trong nó, các tập tin bên trong thư mục này sẽ được bỏ qua. Để hiển thị dung lượng của tất cả tập tin bên trong thư mục, sử dụng tùy chọn -a hoặc –all như sau:
 <br> -  **du -a  FILE**

 ### Lệnh df
**df** báo cáo không gian đã dùng và còn trống của tất các hệ thống tập tin đang được mount trên hệ thống.

Đơn vị mặc định của df là 1024 byte. Chúng ta có thể thay đổi giá trị này bằng cách sử dụng tùy chọn **-B** hay **–block-size** như sau:
<br> - **df -B SIZE FILE**

Mặc định, df chỉ in ra các hệ thống tập tin có kích thước lớn hơn 0, và bỏ qua các hệ thống tập tin có kích thước bằng 0 (những hệ thống tập tin này được gọi là **dummy file system**). Để in ra thông tin của tất cả các hệ thống tập tin đang có, bao gồm các các hệ thống tập tin có kích thước bằng 0, sử dụng tùy chọn **-a** hoặc **–all**.

Để kết quả xuất ra của df dễ hiểu hơn, chúng ta có thể sử dụng tùy chọn **-h** hay **–human-readable**:
