# [Thực hành 1] Ước lượng Story Point với Planning Poker & Thiết lập Sprint Goal

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## 1. Mục tiêu

Trong buổi thực hành này, tôi áp dụng chuỗi Fibonacci sửa đổi (0.5, 1, 2, 3, 5, 8, 13, 20, 40, 100) để ước lượng độ lớn tương đối của User Story dựa trên Story mốc US02. Đồng thời, tôi rèn luyện kỹ năng điều phối Planning Poker khi team có tranh luận và cách viết Sprint Goal đúng chuẩn agile.

- Sử dụng Story mốc US02 (2 points) làm chuẩn so sánh độ phức tạp, rủi ro và nỗ lực.
- Thực hành giải quyết bất đồng điểm số qua thảo luận kỹ thuật thay vì lấy trung bình.
- Xây dựng Sprint Goal tập trung vào giá trị cốt lõi thay vì liệt kê danh sách task.

## 2. Mô tả

Đóng vai trò là thành viên trong Scrum Team của dự án giao đồ ăn 'GoFood', tôi tiến hành ước lượng và lập kế hoạch cho Sprint 1 với 4 User Story đã cho.

- Bối cảnh: Dự án GoFood chuẩn bị khởi động Sprint 1 kéo dài 2 tuần.
- Story mốc làm chuẩn: US02 = 2 points (Là khách hàng, tôi muốn xem danh sách các món ăn kèm giá tiền của từng quán).

## 3. Bước 1 (Ước lượng Story Point)

Dựa trên 3 yếu tố cốt lõi là Độ phức tạp, Rủi ro và Nỗ lực, tôi tiến hành so sánh các User Story còn lại với Story mốc US02 và đưa ra các điểm số Fibonacci phù hợp kèm theo luận điểm giải thích chi tiết.

| User Story | Story Point | Luận điểm so sánh với US02 (2 points) |
| --- | --- | --- |
| US01: Đăng nhập bằng SĐT và mật khẩu | 1 points | Nhỏ hơn US02. Task này chỉ xây dựng form đăng nhập cơ bản và kiểm tra mật khẩu, chưa bao gồm việc tích hợp dịch vụ gửi mã OTP qua SMS bên thứ ba nên độ phức tạp thấp hơn. |
| US02: Xem danh sách món ăn kèm giá | 2 points | Story mốc của đội. Dùng làm chuẩn để so sánh các story khác về mặt UI list và gọi API đơn giản. |
| US03: Tìm kiếm quán ăn qua GPS | 5 points | Lớn hơn US02. Tác vụ này đòi hỏi tích hợp định vị GPS của thiết bị di động, thuật toán tính khoảng cách địa lý theo bán kính và xử lý ngoại lệ khi khách hàng tắt quyền truy cập vị trí. |
| US04: Thanh toán qua Napas / Thẻ quốc tế | 8 points | Lớn hơn US02 đáng kể. Phụ thuộc vào cổng thanh toán bên thứ ba, đòi hỏi xử lý các trạng thái giao dịch phức tạp (thành công, thất bại, pending) và tuân thủ các tiêu chuẩn bảo mật dữ liệu tài chính khắt khe. |

## 4. Bước 2 (Mô phỏng xử lý bất đồng Planning Poker)

Giả sử ở US03, Dev Senior chọn 2 points vì cho rằng việc gọi thư viện GPS có sẵn rất nhanh, trong khi Dev Junior chọn 5 points do lo ngại về các ca biên (edge cases) khi thiết bị mất tín hiệu định vị hoặc người dùng từ chối cấp quyền.

Scrum Master điều phối bằng cách yêu cầu cả hai giải thích góc nhìn kỹ thuật của mình. Sau khi phân tích sâu về rủi ro xử lý ngoại lệ GPS, team thống nhất điều chỉnh và chốt lại con số đồng thuận là 5 points cho US03.

- Không lấy trung bình cộng điểm số các phiếu bầu.
- Tập trung tranh luận dựa trên rủi ro thực tế và độ phức tạp kỹ thuật.

## 5. Bước 3 (Thiết lập Sprint Goal)

Sprint Goal được viết ngắn gọn, tập trung vào giá trị mang lại cho người dùng cuối thay vì liệt kê danh sách các đầu việc (task list) phải làm trong Sprint.

- Câu phát biểu Sprint Goal hoàn chỉnh: 'Giúp khách hàng tìm được quán ăn gần nhất và hoàn thành đơn đặt món ăn đầu tiên thành công'.

## 6. Bước 4 (Phân loại tính năng ngoài mục tiêu)

Nếu Product Owner đề xuất thêm tính năng 'Nhập mã giảm giá khuyến mãi' ngay trong Sprint 1, theo đúng nguyên tắc Scrum, tính năng này không phục vụ trực tiếp cho Sprint Goal hiện tại ('hoàn thành đơn đặt món đầu tiên thành công').

Hướng xử lý: Product Owner sẽ ghi nhận yêu cầu mới này vào Product Backlog, tiến hành sắp xếp lại thứ tự ưu tiên (refinement), và đưa ra cân nhắc thảo luận trong buổi Sprint Planning kế tiếp thay vì nhồi nhét vào Sprint 1 đang chạy.

- Bảo vệ sự tập trung của Scrum Team trong suốt vòng đời Sprint.
- Đảm bảo Product Backlog luôn được cập nhật linh hoạt theo yêu cầu kinh doanh.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `btth1.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
