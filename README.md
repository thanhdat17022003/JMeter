# JMeter
Mô tả:
Sử dụng Apache JMeter để kiểm tra hiệu suất của trang web https://www.history.com/
Đầu tiên, thêm một User (Thread Group) vào Test Plan. Ở User sẽ xác định số lượng người dùng ảo (threads), thời gian khởi động (ramp-up period) và số lần lặp lại (loop count) cho thử nghiệm.
Thêm HTTP Request Sampler: Trong History, thêm một HTTP Request Sampler để xác định các yêu cầu HTTP sẽ được gửi tới trang web Blue Origin. Đặt "Server Name or IP" là "/www.history.com" và "Path" là "/" để gửi yêu cầu tới trang chủ.

![j1](https://github.com/thanhdat17022003/JMeter/assets/148479507/37c84c92-b0a6-4a48-9412-b124e0d0aa3d)

Thêm HTTP Request Sampler tiếp theo là "Destination". Với "Server Name or IP" là "www.blueorigin.com" và "Path" là /destinations/.

![J2](https://github.com/thanhdat17022003/JMeter/assets/148479507/fb128b67-c5cb-43cb-b9ad-80ee158548a8)
Kết quả thu được hiển thị ở "View Results Tree" cho Blue Origin lần lượt:
Thời gian tải: 525 ms
Thời gian kết nối: 370 ms
Độ trễ: 513 ms
Kích thước phản hồi:
Kích thước trong byte: 117 byte
Byte đã gửi: 802 byte
Kích thước tiêu đề trong byte: 160 byte
Kích thước nội dung trong byte: 14 byte
Thông tin bổ sung:
Số lần lấy mẫu: 1
Lỗi: 0
Loại dữ liệu: "text"
Mã phản hồi: 308
Thông báo phản hồi: Permanent Redirect
Kiểu nội dung: text/plain
Mã hóa dữ liệu: null
![J3](https://github.com/thanhdat17022003/JMeter/assets/148479507/fee19b5c-c832-4203-b354-b44a30a92dee)

Đánh giá: hiệu suất trang web history trong lần thử nghiệm 1 được đánh giá là tốt.
Thời gian tải trang: 525 ms là thời gian tải trang khá nhanh, nằm trong mức chấp nhận được.
Kết nối: Thời gian kết nối 370 ms và độ trễ 513 ms cũng nằm trong mức bình thường.
Kích thước phản hồi: Kích thước phản hồi 174 byte là một kích thước nhỏ, giúp giảm thiểu thời gian tải trang.
