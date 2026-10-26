1. AI bỏ sót kiểm thử Trạng thái Giao diện:

Thiếu sót phát hiện: AI chỉ tập trung viết test case luồng chức năng như điền form đúng/sai mà bỏ quên hoàn toàn việc test Loading state (vô hiệu hóa nút khi đang call API).

Cách sửa: Bổ sung thủ công TC07 để kiểm tra trạng thái xoay vòng của nút Lưu, ngăn chặn hành vi click nhiều lần.

2. AI áp dụng sai phạm vi của Business Rule:

Lỗi phát hiện: Khi sinh test case cho quy tắc BR1 ("thời gian phải lớn hơn hiện tại ít nhất 5 phút"), AI đã tự động áp dụng bắt lỗi này cho cả lịch tưới cài đặt ở chế độ Tần suất "Tùy chỉnh" cho những ngày trong tương lai. Điều này sai logic vì Spec chỉ yêu cầu validate điều kiện này "Nếu chọn giờ tưới cho ngày hiện tại".

Cách sửa: Đã sửa lại bằng cách tách thành 2 test case: một cái kiểm tra validate 5 phút cho ngày hôm nay (mong đợi: báo lỗi UI-Error), và một cái cài giờ nhỏ hơn giờ hiện tại nhưng tick chọn ngày mai (mong đợi: lưu thành công).
