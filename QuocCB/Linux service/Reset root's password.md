Bước 1: Trong trình đơn khởi động grub chọn tùy chọn để chỉnh sửa.

<img src=https://i.imgur.com/uf1CWQj.png>

Bước 2: Chọn e và  tìm tới dòng có chữ **ro**

<img src=https://i.imgur.com/IViqgQM.png>

Và thay thế **ro** bằng **rw init=/sysroot/bin/sh**:

<img src=https://i.imgur.com/hXZVvZ2.png>

Bước 3: Sau đó Ctrl+X để bắt đầu và chế độ single user mode.

<img src=https://i.imgur.com/dXuqS10.png>

Bước 4: Bây giờ truy cập vào hệ thống với lệnh này:

> chroot /sysroot

Bước 5: Tạo mật khẩu mới cho tài khoản root.

> passwd root



 Bước 6: Update thông tin vào selinux và thoát khỏi chế độ chroot.

> touch /.autorelabel
<br>exit


Pasword của Root đã được reset thành công!
