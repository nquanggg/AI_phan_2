# Bảng Test Case: Tính năng Lên lịch tưới cây

*Bảng Test Case truy vết yêu cầu (Bao phủ: Biên, Rỗng, Trùng, Quyền và 4 UI States)*

| TC ID | Yêu cầu (Trace) | Tiêu đề | Điều kiện tiên quyết | Các bước thực hiện | Kết quả mong đợi | Loại Test |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC01 | UI-Empty | Kiểm tra hiển thị màn hình khi chưa có lịch tưới  | Tài khoản mới tinh, chưa tạo lịch nào | 1. Mở tab "Lịch tưới" | Hiển thị ảnh minh họa cây khô và nút "Tạo lịch tưới đầu tiên" | UI / Rỗng |
| TC02 | BR1, UI-Error | Kiểm tra tạo lịch tưới với giờ tưới trong quá khứ | Đang ở màn hình Tạo lịch | 1. Nhập Tên: "Cây Kim Tiền"<br>2. Chọn giờ tưới < giờ hiện tại<br>3. Bấm Lưu | Trường Giờ tưới báo lỗi text đỏ: "Thời gian phải lớn hơn hiện tại ít nhất 5 phút" | Biên (Thời gian) |
| TC03 | Input Valid | Kiểm tra nhập Tên cây đúng 50 ký tự | Đang ở màn hình Tạo lịch | 1. Nhập Tên cây gồm đúng 50 chữ cái<br>2. Nhập các trường hợp lệ<br>3. Bấm Lưu | Lưu thành công, chuyển về màn hình danh sách | Biên  |
| TC04 | Input Invalid | Kiểm tra nhập Tên cây 51 ký tự | Đang ở màn hình Tạo lịch | 1. Paste đoạn text 51 ký tự vào Tên cây | Hệ thống chặn không cho gõ ký tự thứ 51  | Biên (Ký tự) |
| TC05 | BR2 | Kiểm tra tạo lịch bị trùng lặp dữ liệu | Đã có lịch: "Hoa Hồng", 08:00, Hàng ngày | 1. Tạo lịch mới y hệt lịch cũ<br>2. Bấm Lưu | Hiển thị popup lỗi: "Lịch tưới này đã tồn tại" | Trùng lặp |
| TC06 | Quyền | Kiểm tra quyền truy cập tạo lịch khi chưa đăng nhập  | App chưa đăng nhập | 1. Bấm nút "Tạo lịch tưới" | Chuyển hướng sang màn hình Yêu cầu Đăng nhập | Quyền |
| TC07 | UI-Loading | Kiểm tra trạng thái hệ thống khi đang xử lý  | Đang ở màn hình Tạo lịch | 1. Nhập thông tin hợp lệ<br>2. Bấm Lưu | Nút Lưu hiển thị spinner xoay vòng, không thể bấm đúp 2 lần | UI |