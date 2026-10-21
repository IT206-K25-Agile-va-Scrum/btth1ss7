# [Thực hành 1] Ước lượng Story Point với Planning Poker & Thiết lập Sprint Goal - Dự án GoFood

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## Nhiệm vụ 1: Ước lượng Story Point với Planning Poker

Trong buổi Planning của Sprint 1 (thời lượng 2 tuần) cho dự án giao đồ ăn GoFood, Scrum Team tiến hành ước lượng độ lớn tương đối của các User Story dựa trên chuỗi Fibonacci sửa đổi (0.5, 1, 2, 3, 5, 8, 13, 20, 40, 100). Đội chọn US02 làm Story mốc với mức định giá là 2 points.

Dựa trên ba yếu tố cốt lõi gồm Độ phức tạp (Complexity), Rủi ro (Risk) và Nỗ lực (Effort), tôi đã cùng đội ngũ phân tích và đưa ra các mức điểm cho từng User Story trong Product Backlog như sau:

- Nguyên tắc cốt lõi: Story Point là thước đo tương đối của riêng Scrum Team, không quy đổi cứng nhắc thành số giờ công (hours).
- Không tính điểm trung bình các phiếu biểu quyết, mọi con số đều phải thông qua tranh luận kỹ thuật để tìm ra tiếng nói chung.

| Mã User Story | Tên User Story | Story Point | Lập luận so sánh với Story mốc (US02 = 2 points) |
| --- | --- | --- | --- |
| US01 | Đăng nhập bằng số điện thoại và mật khẩu | 1 point | Nhỏ hơn US02 vì tính năng này chỉ bao gồm giao diện form nhập liệu cơ bản và kiểm tra chuỗi ký tự mật khẩu trong cơ sở dữ liệu, chưa bao gồm luồng phức tạp tích hợp cổng gửi mã OTP qua SMS bên thứ ba. |
| US02 | Xem danh sách món ăn kèm giá tiền | 2 points | Đây là Story mốc chuẩn của đội (Reference Story). Mức độ phức tạp trung bình khi vừa render danh sách dạng lưới, vừa xử lý hiển thị giá tiền và hình ảnh món ăn. |
| US03 | Tìm kiếm quán ăn qua GPS xung quanh vị trí | 3 points | Lớn hơn US02 do có độ phức tạp cao hơn về mặt thuật toán tính toán khoảng cách địa lý dựa trên tọa độ vĩ độ/kinh độ, tích hợp API định vị GPS của thiết bị và xử lý ngoại lệ khi khách hàng tắt quyền định vị. |
| US04 | Thanh toán đơn hàng qua Napas/Thẻ quốc tế | 8 points | Lớn hơn US02 đáng kể bởi rủi ro kỹ thuật rất cao, phụ thuộc vào việc tích hợp các cổng thanh toán bên thứ ba (Sandbox/Production), xử lý callback, bảo mật thông tin tài chính và các tình huống giao dịch lỗi/timeout. |

## Nhiệm vụ 2: Mô phỏng xử lý bất đồng Planning Poker

Trong quá trình biểu quyết cho US03 (Tìm kiếm quán ăn qua GPS), Dev Senior giơ thẻ 2 points vì cho rằng team đã có sẵn thư viện tính toán khoảng cách haversine từ project cũ, trong khi Dev Junior giơ thẻ 5 points do lo ngại về độ trễ khi lấy tọa độ GPS thực tế trên các dòng máy Android đời cũ và việc xử lý màn hình hiển thị khi không có kết nối mạng.

Scrum Master ngay lập tức can thiệp bằng cách yêu cầu cả hai lập luận rõ lý do. Dev Senior giải thích về thư viện sẵn có, còn Dev Junior chỉ ra các edge cases về phần cứng và quyền truy cập vị trí.

Sau khi thảo luận làm rõ các rủi ro mà Dev Junior nêu ra, toàn team nhận ra phần xử lý ngoại lệ GPS tốn sức hơn tưởng tượng và đi đến đồng thuận chốt lại con số 3 points cho US03.

- Scrum Master giữ vai trò điều phối trung lập, không áp đặt ý kiến.
- Mục đích của việc tranh luận là để chia sẻ góc nhìn kỹ thuật và làm rõ yêu cầu (Acceptance Criteria), không phải thắng thua.

## Nhiệm vụ 3: Thiết lập Sprint Goal

Câu phát biểu Sprint Goal cho Sprint 1 được xây dựng theo đúng nguyên tắc tập trung vào giá trị cốt lõi, hướng tới việc giúp khách hàng hoàn thành luồng nghiệp vụ mua hàng đầu tiên:

'Giúp khách hàng tìm được quán ăn gần nhất, xem menu và hoàn thành đơn đặt món ăn đầu tiên thành công.'

- Sprint Goal này đóng vai trò kim chỉ nam, giúp Scrum Team từ chối các tính năng lan man không phục vụ trực tiếp cho việc đặt món.
- Không viết Sprint Goal dưới dạng liệt kê danh sách các công việc hay User Story rời rạc.

## Nhiệm vụ 4: Phân loại tính năng ngoài mục tiêu

Nếu trong quá trình Sprint 1 đang diễn ra, Product Owner (PO) hoặc Stakeholder yêu cầu bổ sung ngay tính năng 'Nhập mã giảm giá khuyến mãi', hướng xử lý của Scrum Team sẽ tuân thủ nghiêm ngặt các nguyên tắc của Scrum như sau:

Thứ nhất, tuyệt đối không đưa tính năng mã giảm giá vào Sprint 1 hiện tại vì sẽ làm thay đổi Sprint Backlog, gây quá tải cho đội ngũ và phá vỡ Sprint Goal đã cam kết.

Thứ hai, Product Owner sẽ tiếp nhận yêu cầu, viết lại thành User Story hoàn chỉnh và đưa vào Product Backlog, sau đó tiến hành sắp xếp lại thứ tự ưu tiên (Refinement).

Thứ ba, tính năng này sẽ được đưa ra thảo luận và cân nhắc đưa vào Sprint Planning của Sprint kế tiếp (Sprint 2) dựa trên dung lượng (Velocity) của đội.

- Bảo vệ sự ổn định của Sprint Goal là trách nhiệm của Scrum Master và toàn đội.
- Product Backlog là nơi linh hoạt tiếp nhận mọi thay đổi, nhưng Sprint Backlog trong chu kỳ Sprint là bất khả xâm phạm trừ khi hủy Sprint.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `btth1.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
