## Types of Database Management Systems

Có một số loại **Hệ quản trị cơ sở dữ liệu**. Dưới đây là 7 DBMS thông dụng:
1. Hierarchical databases
2. Network databases
3. Relational databases
4. Object-oriented databases
5. Graph databases
6. ER model databases
7. Document databases
8. NoSQL databases

### Hierarchical databases

Trong một mô hình **Hierarchical Databases Management Systems (Hierarchical DBMSs)**, dữ liệu được lưu trữ trong các **node** quan hệ cha-con.
Trong một **hierarchical database**, bên cạnh dữ liệu thực tế, các bản ghi cũng chứa thông tin về các nhóm của chúng về các mối quan hệ cha con.

Trong một mô hình hierarchical database, dữ liệu được tổ chức thành một cấu trúc hình cây.
Dữ liệu này được lưu trữ dưới dạng tập hợp của các trường, mỗi trường chỉ chứa một giá trị.
Các bản ghi được liên kết với nhau qua các liên kết trong mối quan hệ cha-con.
Trong một mô hình hierarchical database, mỗi bản ghi con có duy nhất một cha.
Một cha có thể có nhiều con.

Để truy xuất dữ liệu của một trường chúng ta cần xét kỹ từng cây cho tới khi bản ghi được tìm thấy.

Cấu trúc của hệ thống **hierarchical database** đã được phát triển bởi **IBM** vào đầu những năm 1960.
Cấu trúc hierarchical đơn giản, nó không linh hoạt do mối quan hệ cha-con one-to-many. các Hierarchical databases được sử dụng rộng rãi để xây dựng các ứng dụng có hiệu suất và khả năng ứng dụng cao, thường được sử dụng trong ngân hàng và ngày công nghiệp viễn thông.

**IBM Information Management System (IMS)** và **Windows Registry** là hai ví phổ biết của **hierarchical databases**

<img src=https://www.c-sharpcorner.com/UploadFile/65fc13/types-of-database-management-systems/Images/Types%20of%20Database%20Management%20Systems2.jpg>  <img src=https://www.c-sharpcorner.com/UploadFile/65fc13/types-of-database-management-systems/Images/Types%20of%20Database%20Management%20Systems3.jpg>

* **Ưu điểm**:
Hierarchical database có thể được truy cập và cập nhật nhanh chóng bởi vì trong cấu trúc mô hình này giống một cái cây và các mối quan hệ giữa các bản ghi được xác định trước. Tính năng này có hai mặt.

* **Nhược điểm**:
Loại cấu trúc cơ sở dữ liệu này là mỗi **con** trong **cây** chỉ có thể có duy nhất một **cha**, và các mối quan hệ hay sự liên kết giữa các **con** là không được phép. Có thể thêm một trường hoặc bản ghi mới nhưng yêu cầu định nghĩa lại toàn bộ cơ sở dữ liệu

### Network Databases

**Network Database Management Systems (Network DBMSs)** sử dụng một cấu trúc mạng để tạo quan hệ giữa các thực thể.
**Network databases** được sử dụng chủ yếu trên các máy tính kỹ thuật số lớn.
**Network databases** là **Hierarchical data** nhưng khác **Hierarchical databases** ở chỗ một node chỉ có thể có một **parent**, một **node** mạng có thể có quan hệ với nhiều thực thể. Một **Network database** trông giống một mạng nhện hơn.

Trong **Network databases*, các **con** được gọi là các thành viên và các **cha** được gọi là **occupier**. Sự khác nhau giữa các **child** hay **member** có thể có nhiều hơn một **parent**.

<img src=https://www.c-sharpcorner.com/UploadFile/65fc13/types-of-database-management-systems/Images/Types%20of%20Database%20Management%20Systems4.jpg>

Dữ liệu trong **Network Database** được tổ chức theo quan hệ many-to-many.

Cấu trúc **Network Database** được phát minh bởi Charles Bachman. Một số **Network Database** thông dụng là Integrated Data Store (IDS), Integrated Database Management System (IDMS), Raima Database Manager, TurboIMAGE, and Univac DMS-1100.

## Relational Database

RDBMS là viết tắt của Relational Database Management System (Hệ thống quản lý cơ sở dữ liệu quan hệ), Tất cả các hệ thống quản lý cơ sở dữ liệu hiện đại như SQL, MS SQL Server, ORACLE, … là dựa trên RDBMS. Nó được gọi là RDBMS bởi vì nó dựa trên Relational Model (Mô hình quan hệ) đã được giới thiệu bởi E.F.Codd.

Trong RDBMS, dữ liệu được biểu diễn bởi các hàng.
Relational Database là cơ sở dữ liệu được sử dụng phổ biến nhất.
Nó chứa các bảng và mỗi bảng có Primary Key riêng.
Bởi vì các bảng này được tổ chức chặt chẽ nên việc truy cập dữ liệu trở nên dễ dàng hơn trong RDBMS.

* **Bảng (table)**.

RDBMS sử dụng các bảng để lưu trữ dữ liệu.
Một bảng là một tập hợp các dữ liệu có liên quan và chứa các hàng và các cột để lưu dữ liệu.
Một bảng là một kho lưu trữ (Storage) dữ liệu đơn giản nhất trong RDBMS.
<br> Ví dụ:

| ID |  TEN    | TUOI|  KHOAHOC  | HOCPHI |
|----|---------|-----|-----------|--------|
|  1 | Hoang   |  21 | CNTT      |  4     |
|  2 | Viet    |  19 | DTVT      |  3.0   |
|  3 | Thanh   |  18 | KTDN      |  4     |
|  4 | Nhan    |  19 | CK        |  4.5   |
|  5 | Huong   |  20 | TCNH      |  5     |

* **Field (Trường)**.

Trường, là một thực thể nhỏ nhất của bảng, chứa thông tin cụ thể về mỗi bản ghi trong bảng.
Trong ví dụ trên, trường trong bảng **sinh viên** là **ID**, **TEN**, **TUOI**, **KHOAHOC**, **HOCPHI**.

* **Hàng hoặc Record**.

Một hàng của một bảng cũng được gọi là **record**. Nó chứa thông tin cụ thể về một entry riêng rẽ trong bảng.
Hàng là một thực thể nằm ngang trong bảng.
Bảng **Sinh viên** ở trên có 5 hàng.

* **Cột**.

Một cột là một thực thể dọc trong bảng, chứa tất cả thông tin được liên kết với trường cụ thể trong một bảng. Trong bảng **Sinh viên**, cột **TEN** bao gồm thông tin về tên của sinh viên.

* **Giá trị NULL**

Giá trị **NULL** của một bảng xác định rằng trường đã bị để trống trong khi tạo record.
Nó khác hoàn toàn với giá trị **0** hoặc một trường mà chứa khoảng trống (space).

## Object-Oriented Model

Đây là hệ thống hỗ trợ lưu trữ loại dữ liệu mới hiện nay.
Trong đó, dữ liệu được lưu trữ dưới dạng đối tượng (Object).
Những đối tượng (Object) này có thuộc tính như giới tính, tuổi tác, v…v và những phương thức để xác định dữ liệu được dùng làm gì.
Một ví dụ cho kiểu hệ thống quản lý cơ sở dữ liệu theo kiểu đối tượng là PostgreSQL.


## NoSQL Databases.

NoSQL là một danh mục mới của Hệ thống quản lý cơ sở dữ liệu. Thuộc tính chính của NoSQL là không phụ thuộc vào khái niệm của Cơ sở dữ liệu quan hệ. Do đó, NoSQL nghĩa là “Không chỉ SQL” (Not only SQL).

Khái niệm của cơ sở dữ liệu NoSQL phát triển cùng với những ông lớn của ngành công nghệ trực tuyến với một khối lượng khổng lồ các dữ liệu cần xử lý như Google, Facebook, Amazone, v..v.

Cụ thể, khi bạn sử dụng cơ sở dữ liệu quan hệ với một lượng dữ liệu không lồ, hệ thống sẽ bắt đầu có dấu hiệu phản hồi chậm hơn.
Để giải quyết tình trạng này, hiển nhiên chúng ta có thể nâng cấp những phần cứng hiện tại của hệ thống.
Tuy nhiên, một phương án khác cho tình trạng này là phân phối cơ sở dữ liệu trên các host khác nhau để tăng tốc độ truyền tải.. 
Cơ sở dữ liệu NoSQL là những cơ sở dữ liệu “không quan hệ” và có thể nhận rộng tốt hơn cơ sở dữ liệu dang quan hệ.
Hệ thống này không sử dụng SQL để xử lý dữ liệu, và cũng không tuân theo một cách khắc khe lược đồ (schema) như trong mô hình quan hệ
