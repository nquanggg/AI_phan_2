# Spec: Tính năng Lên lịch tưới cây

## Mục đích: Cho phép người dùng tạo lịch nhắc nhở tưới nước cho từng loại cây.

## Input:

1. Tên cây (Text input): Bắt buộc, tối đa 50 ký tự. Không được chứa ký tự đặc biệt (chỉ chấp nhận chữ cái, số và khoảng trắng).

2. Tần suất (Dropdown): Hàng ngày, Hàng tuần, Tùy chỉnh (chọn thứ trong tuần).

3. Giờ tưới (Time picker): Định dạng HH:MM (24h).

## Quy tắc:

1. BR1: Nếu chọn giờ tưới cho ngày hiện tại, thời gian phải lớn hơn thời gian hiện tại của thiết bị ít nhất 5 phút.

2. BR2: Không cho phép tạo 2 lịch tưới trùng toàn bộ (Tên cây - Tần suất - Giờ tưới).

## Trạng thái giao diện:

1. Empty: Khi chưa có lịch nào, hiển thị ảnh minh họa cây khô và nút "Tạo lịch tưới đầu tiên".

2. Loading: Khi nhấn "Lưu", nút chuyển sang trạng thái xoay vòng, vô hiệu hóa các thao tác khác.

3. Ideal: Hiển thị danh sách lịch tưới dưới dạng thẻ (card).

4. Error: Hiển thị text màu đỏ dưới trường nhập liệu nếu vi phạm validate.

# Danh sách câu hỏi còn mơ hồ (gửi BA):

 * Với tần suất "Tùy chỉnh", nếu người dùng không chọn bất kỳ thứ nào trong tuần thì hệ thống có báo lỗi ngay lúc chọn hay đợi bấm nút Lưu? 

 * Nếu người dùng thay đổi múi giờ trên điện thoại, lịch tưới cố định theo múi giờ cũ hay tự động cập nhật theo múi giờ mới?

 * Nếu Tên cây bị trùng nhưng khác Tần suất, hệ thống có cảnh báo để tránh người dùng nhầm lẫn không?