## Time
- Hướng dẫn xem ngày trên hệ thống
>date

- Để biết thêm các options thì dùng lệnh
>man date

- Để kiểm tra múi giờ
> cd /usr/share/zoneinfo/
<br>ls

- Để chỉnh thời gian theo múi giờ
> cp /usr/share/zoneinfo/Asia/Ho_Chi_Minh /etc/localtime

- Hướng dẫn cấu hình đồng bộ bằng ntp
  - Cài đặt ntp
>yum -y install ntp

  - Cấu hình cho ntp chạy khi khởi động
> chkconfig ntpd on

  - Khởi động ntp
> service ntpd start

  - Kiểm tra ntp làm việc
> ntpq -p

- Cập nhật một server khác
>ntpdate –q <địa chỉ time_server>

- Cài đặt giờ theo ý muốn<br>
  - Cài đặt ngày/tháng/năm:
> date +%Y%m%d -s "20150101"

  - Cài đặt giờ/phút/giây:
> date +%T -s "12:00:00"
