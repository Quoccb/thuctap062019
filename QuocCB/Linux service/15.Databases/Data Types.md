## MySQL Data Types

Một bảng cơ sở dữ liệu chứa nhiều cột với các kiểu dữ liệu khác nhau như số hoặc ký tự.
MySQL cung cấp thêm các kiểu dữ liệu khác, khổng chỉ số hay ký tự.


### MySQL Numeric Data Types

Trong MySQL, bạn có thể thấy tất các kiểu dữ liệu kiểu số chuẩn SQL bao gồm kiểu dữ liệu chính xác và các kiểu dữ liệu xấp xỉ như **integer**, **fixed-poit** and **floating poit**.
Mặt khác, MySQL cũng có kiểu dữ liệu **BIT** để chứa các giá trị bit. Các kiểu số có thể có dấu hoặc không dấu trừ kiểu **BIT**.

Ta có bảng tóm tắt các kiểu dữ liệu kiểu số trong MySQL.

| Numeric Types     | Description     |
| :------------- | :------------- |
| TINYINT  | Số nguyên rất nhỏ       |
| SMALLINT | Số nguyên nhỏ |
| MEDIUMINT| Số nguyên vừa |
| INT       | Số nguyên tiêu chuẩn |
| BIGINT | Số nguyên lớn |
| DECIMAL | Số fixed-point |
| FLOAT | |
| DOUBLE | |
| BIT | |

### MySQL Boolean Data Type

MySQL không có sẵn kiểu dữ liệu **BOOLEAN** hay **BOOL**. Để biểu diễn các giá trị **Boolean**, MySQL sử dụng kiểu số nguyên nhỏ nhất là TINYINT(1). Nói cách khác, **BOOLEAN** và **BOOL** là tương đương với **TINYINT(1)**.

### MySQL String Data Types

Trong MySQL, một chuỗi có thể chứa bất cứ thứ gì từ văn bản rõ đến các dữ liệu nhị phân như các ảnh hay file. Các chuỗi có thể só sánh và tìm kiếm dựa trên mô hình **matching** bằng cách sử dụng toán tử **LIKE**, **regular expression** và **full-text search**.

Ta có bảng tóm tắt các kiểu dữ liệu chuỗi trong MySQL:

| String Types | Description     |
| :------------- | :------------- |
| CHAR       | Được dùng để thể hiện chuỗi có độ dài cố định, có thể chứa các chữ số, chữ cái và các ký tự đặc biệt. Kích cỡ của nó khoảng 0 - 255 ký tự. Mặc định là 1. |
| VARCHAR | Được dùng để xác định một chuỗi có độ dài thay đổi (variable length string), có thể chứa chữ số, chữ cái và các ký tự đặc biệt. Kích cỡ của nó khoảng 0 - 65535 ký tự |
| BINARY | Bằng với CHAR nhưng chứa chuỗi byte nhị phân.  |
| VARBINARY | Tương tự VARCHAR nhưng chứa chuỗi byte nhị phân |
| TEXT(Size) | Chứa một chuỗi có thể chứa chiều dài tối đa 255 ký tự |
| TINYTEXT | |
| MEDIUMTEXT | |
| LONGTEXTv | |
| ENUM(val1, val2, val3,...)| |
| SET( val1,val2,val3,....) | |
| BLOB(size) | |

### MySQL date and time data types

MySQL cung cấp các kiểu cho date và time cũng như tổng hợp của date và time. Mặt khác, MySQL hỗ trợ kiểu dữ liệu *timestamp* để theo dõi những thay đổi trong một hàng của một bảng. Nếu bạn chỉ muốn lưu trữ năm mà không quan tâm tới ngày và tháng, bạn có thể sử dụng kiểu dữ liệu **YEAR**.

| Date and Time Types | Description     |
| :------------- | :------------- |
| DATE        | Một giá trị date có định dạng **CCYY-MM-DD**       |
| TIME | Một giá trị time có định dạng **hh:mm:ss** |
| DATETIME | Một giá trị date và time có định dạng **CCYY-MM-DD hh:mm:ss** |
|TIMESTAMP | Một giá trị timestamp có định dạng CCYY-MM-DD hh:mm:ss** |
| YEAR | | Một giá trị year có đị dạng CCYY hoặc YY |


### MySQL spatial data types

MySQL hỗ trợ nhiều kiểu dữ liệu không gian chứa các kiểu giá trị hình học, địa lý khác nhau.

| Spatial Data Types | Description     |
| :------------- | :------------- |
| GEOMETRY       | Một giá trị không gian của bất kỳ loại nào       |
| POINT | Một điểm tọa độ (một cặp tọa độ X-Y) |
| LINESTRING | Một đường cong (một hoặc nhiều giá trị **POINT**) |
| POLYGON | Một hình đa giác |
| GEOMETRYCOLLECTION | Một tập hợp các giá trị **GEOMETRY** |
| MULTILINESTRING | Một tập hợp các LINESTRING |
| MULTIPOINT | Một tập hợp các POINT |
| MULTIPOLYGON | Một tập hợp các POLYGON |
