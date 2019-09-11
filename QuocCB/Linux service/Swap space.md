### Tạo phân vùng Swap trên CentOS

Khi máy tính cần chạy những chương trình lớn hơn khả năng có thể của bộ nhớ vật lý (RAM), hệ điều hành sẽ sử dụng một công nghệ có tên gọi swapping.
Nói nôm na thì công nghệ này sẽ dùng đến những mảng bộ nhớ tạm được lưu trên đĩa cứng, trong khi phần dữ liệu khác vẫn được chuyển vào RAM.
Công nghệ này giúp bạn quản lý việc hoán đổi (swapping) tốt hơn cũng như tăng hiệu năng sử dụng.

Linux chia bộ nhớ vật lý thành các pages.
swapping là một tiến trình thực hiện việc copy một page của bộ nhớ đến một không gian đã được cấu hình trước trên đĩa cứng (gọi là swap space), để giải phóng các pages của bộ nhớ.
Tổng dung lượng của RAM và không gian hoán đổi (swap space) chính là tổng số bộ nhớ ảo (virtual memory).
