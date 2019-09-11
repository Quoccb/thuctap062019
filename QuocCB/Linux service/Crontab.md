### Crontab

- **Cronjob**: Cronjob là các lệnh thực thi hành động đặt trước vào thời điểm nhất định.
Crontab là nơi lưu trữ các Cronjob.
- **Cron** là một tiện ích giúp lập lịch chạy những dòng lệnh bên phía server để thực thi một hoặc nhiều công việc nào đó theo thời gian được lập sẵn.
Một só người gọi những công việc đó là Cron job hoặc Cron task.

- **Cron** là một chương trình deamon, tức là nó được chạy ngầm mãi mãi một khi nó được khởi động lên.
Như các deamon khác thì bạn cần khởi động lại nó nếu như có thay đổi thiết lập gì đó.
Chương trình này nhìn vào file thiết lập có tên là crontab để thực thi những task được mô tả ở bên trong.

### Cron hoạt động như thế nào?

Một cron schedule đơn giản là một text file.
Mỗi người dùng có một cron schedule riêng, file này thường nằm ở */var/spool/cron.*
Crontab files không cho phép bạn tạo hoặc chỉnh sửa trực tiếp với bất kỳ trình text editor nào, trừ phi bạn dùng lệnh crontab.

Một số lệnh thường dùng:

- crontab -e: tạo hoặc chỉnh sửa file crontab.
- crontab -l: hiển thị file crontab.
- crontab -r: xóa file crontab.

### Cài đặt Crontab.
Hầu hết các VPS/Server đều được cài đặt sẵn *Crontab*.
Tuy nhiên vẫn có trường hợp VPS không có.

Để cài đặt Crontab sử dụng lệnh:
> yum install cronie

Start crontab và tự động chạy mỗi khi reboot:

>service crond start

>chkconfig crond on

### Cấu trúc của Crontab.
Crontab có 5 trường xác định thời gian, cuối cùng là lệnh sẽ được chạy định kỳ.
Cấu trúc như sau:
<img src=https://vinahost.vn/uploads/8/tincongnghe/cron-job.jpg>

### Disable email
Mặc định cron gửi email cho người thực thi cron job, nếu bạn muốn tắt chức năng gửi email này đi thì hãy thêm đoạn sau vào cuối dòng

>\>/dev/null 2>&1

Ví dụ:

>0 15 * * 1,4 sh /etc/backup.sh >/dev/null 2>&1
