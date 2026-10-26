# Danh sách Bug Report chuẩn hóa (giả định trên App mẫu):

## BUG 001: App bị crash văng ra ngoài khi dán (paste) 500 ký tự vào trường "Tên cây"

* Môi trường: Android 13, App v1.0.1 (Staging)

* Các bước tái hiện:

1. Vào màn hình Tạo lịch tưới.

2. Copy một đoạn văn bản dài 500 ký tự.

3. Dán vào trường "Tên cây".

* Kết quả thực tế: App lập tức bị đơ 2 giây rồi văng ra màn hình chính của điện thoại .

* Kết quả mong đợi: Hệ thống chỉ nhận 50 ký tự đầu tiên hoặc hiển thị text báo lỗi "Tên cây không vượt quá 50 ký tự" (UI-Error state).

## BUG 002: Không hiển thị trạng thái "Empty" khi người dùng xóa hết lịch tưới

* Môi trường: iOS 16, App v1.0.1 (Staging)

* Các bước tái hiện:

1. Đăng nhập vào tài khoản đang có 1 lịch tưới.

2. Thực hiện thao tác xóa lịch tưới duy nhất đó.

3. Quan sát màn hình Lịch tưới.

* Kết quả thực tế: Màn hình không có nội dung gì.

* Kết quả mong đợi: Phải hiển thị trạng thái Empty (Ảnh minh họa cây khô + nút "Tạo lịch tưới đầu tiên").

## BUG 003: Lưu trùng lịch tưới bị ghi đè im lặng, không có cảnh báo

* Môi trường: Web App, Chrome Version 115

* Các bước tái hiện:

1. Chọn một lịch tưới đã có sẵn (Ví dụ: Cây Cau, 09:00, Hằng ngày).

2. Tạo mới một lịch có thông tin giống hệt 100%.

3. Bấm Lưu.

* Kết quả thực tế: Hệ thống lưu thành công, quay về màn hình danh sách chỉ thấy 1 lịch tưới (lịch mới đã ghi đè lịch cũ dưới database).

* Kết quả mong đợi: Hệ thống chặn không cho lưu và hiển thị thông báo lỗi "Lịch tưới này đã tồn tại".