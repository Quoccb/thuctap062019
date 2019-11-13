## Database
Database là một tập hợp có hệ thống của **Data**. Các **Database** hỗ trợ lưu trữ và thao tác với dữ liệu. Các **Database** làm việc quản lý dữ liệu trở nên dễ dàng hơn.
<br>Ví dụ một danh bạ điện thoại trực tuyến sẽ sử dụng **database** để chứa dữ liệu liên quan đến người, số điện thoại, các thống tin liên lạc khác,...
<br>Cơ quan điện lực cũng sử dụng một cơ sở dữ liệu để quản lý hóa đơn, các vấn đề liên quan đến khách hàng, xử lý dữ liệu lỗi,...
<br>Facebook cũng thế, nó cần chứa, thao tác và trình bày dữ liệu liên quan đến các  thành viên, bạn bè của họ, các hoạt động của các thành viên, các tin nhắn, các chương trình quảng cáo,... và nhiều thứ nữa.

## Database Managment System (DBMS).
**Hệ quản trị cơ sở dữ liệu** có thể hiểu là hệ thống được thiết kế để quản lí một khối lượng dữ liệu nhất định một cách tự động và có trật tự.
Các hành động quản lý này bao gồm chỉnh sửa, xóa, lưu thông tin và tìm kiếm (truy xuất thông tin) trong một nhóm dữ liệu nhất định.
<br> Nói một cách dễ hiểu hơn, hệ quản trị cơ sở dữ liệu là hệ thống tự động giúp người dùng có thể kiểm soát các thông tin, tạo, cập nhật và diu trì các CSDL.
Trong đó, hai thành phần chính trong một hệ quản trị cơ sở dữ liệu là: Bộ xử lí truy vấn (bộ xử lí yêu cầu) và bộ quản lí dữ liệu.

Hệ quản trị cơ sở dữ liệu có các chức năng chính như sau:
- **Cung cấp môi trường tạo lập cơ sở dữ liệu:** Hệ quản trị CSDL đóng vai trò cung cấp cho người dùng một ngôn ngữ định nghĩa dữ liệu để mô tả, khai báo kiểu dữ liệu, các cấu trúc dữ liệu.<br>
- **Cung cấp cách cập nhật và khai thác dữ liệu:** Hệ quản trị CSDL cung cấp cho người dùng ngôn ngữ thao tác dữ liệu để diễn tả các yêu cầu, các thao tác cập nhật và khai thác cơ sở dữ liệu. Thao tác dữ liệu bao gồm: Cập nhật (nhập, sửa, xóa dữ liệu). Khai thác (tìm kiếm, kết xuất dữ liệu).
<br>
- **Cung cấp các công cụ kiểm soát, điều khiển các truy cập vào cơ sở dữ liệu:** nhầm đảm bảo thực hiện một số yêu cầu cơ bản của hệ cơ sở dữ liệu. Bao gồm:
 1. Đảm bảo an ninh, phát hiện và ngăn chăn các truy cập bất hợp pháp.
 2. Duy trì tính nhất quán của dữ liệu.
 3. Tổ chức và điều khiển các triu cập.
 4. Khôi phục cơ sở dữ liệu khi có sự cố về phần cứng hay phần mềm.
 5. Quản lí các mô tả dữ liệu.


 Hệ thống quản lý cơ sở dữ liệu không phải là một khái niệm mới, nó đã được triển khai lần đầu tiên vào những năm 1960.

 **Intergrated Data Store (IDS)** của **Charles Bachmen** được cho là **DBMS** đầu tiên trong lịch sử.


## SQL
**Structured Query Language (SQL)** - đọc là "S-Q-L" hoặc là "See-Quel" - Là ngôn ngữ chuẩn để làm việc với Cơ sở dữ liệu kiểu quan hệ. Những phần mềm SQL sẽ giúp các thao tác cơ bản với cơ sở dữ liệu như Chèn, Tìm kiếm, Cập nhật, Xóa hiệu quả hơn.

Ngoài những thao tác cơ bản đó, SQL còn đóng vai trò quan trọng trong việc Tối ưu và Bảo trì cơ sở dữ liệu.

Các cơ sở dữ liệu dạng quan hệ như **MySQL Database**, **Oracle**, **Ms SQL server**, **Sybase** đều sử dụng SQL.

Cú pháp của SQL sử dụng trong những cơ sở dữ liệu này gần giống nhau.

## NoSQL

NoSQL là một danh mục mới của Hệ thống quản lý cơ sở dữ liệu. Thuộc tính chính của NoSQL là không phụ thuộc vào khái niệm của Cơ sở dữ liệu quan hệ. Do đó, NoSQL nghĩa là “Không chỉ SQL” (Not only SQL).

Khái niệm của cơ sở dữ liệu NoSQL phát triển cùng với những ông lớn của ngành công nghệ trực tuyến với một khối lượng khổng lồ các dữ liệu cần xử lý như Google, Facebook, Amazone, v..v.

Cụ thể, khi bạn sử dụng cơ sở dữ liệu quan hệ với một lượng dữ liệu không lồ, hệ thống sẽ bắt đầu có dấu hiệu phản hồi chậm hơn.
Để giải quyết tình trạng này, hiển nhiên chúng ta có thể nâng cấp những phần cứng hiện tại của hệ thống.
Tuy nhiên, một phương án khác cho tình trạng này là phân phối cơ sở dữ liệu trên các host khác nhau để tăng tốc độ truyền tải..
Cơ sở dữ liệu NoSQL là những cơ sở dữ liệu “không quan hệ” và có thể nhận rộng tốt hơn cơ sở dữ liệu dang quan hệ.
Hệ thống này không sử dụng SQL để xử lý dữ liệu, và cũng không tuân theo một cách khắc khe lược đồ (schema) như trong mô hình quan hệ
