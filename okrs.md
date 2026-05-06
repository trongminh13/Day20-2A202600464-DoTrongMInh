
# TÀI LIỆU CHIẾN LƯỢC SẢN PHẨM: DOMIN-H FAMILY
**Dự án:** Ứng dụng AI-Mediator Quản lý Tài chính Sinh viên dành cho Phụ huynh  
**Người phụ trách (Product/AI Lead):** Jimala  
**Trạng thái:** Bản nháp V1.0 (Dành cho Investor Pitch & Internal Alignment)

---

## WORKSHOP 3: THIẾT LẬP MỤC TIÊU VÀ KẾT QUẢ THEN CHỐT (OKR - GIAI ĐOẠN NOW)

### 1. Triết lý đo lường (Measurement Philosophy)
Trong quý đầu tiên ra mắt (Q3/2026), DOMIN-H Family không tập trung vào các "Vanity Metrics" (Chỉ số ảo) như số lượt tải app (Downloads) hay số lượt tạo tài khoản. Chúng ta tập trung toàn lực vào việc chứng minh 3 giả thuyết sống còn của một startup B2C: **Sự hình thành thói quen (Habit), Khả năng kiếm tiền (Monetization), và Mức độ gắn kết (Retention).**

---

### 2. Objective (Mục tiêu truyền cảm hứng)

> **"Biến DOMIN-H Family thành 'Giám đốc tài chính' mẫn cán của gia đình: Mang lại sự an tâm tuyệt đối cho cha mẹ, và trả lại sự tự do tài chính minh bạch cho con cái."**

*   **Tại sao chọn Objective này?** Mục tiêu này mang tính định tính và truyền cảm hứng. Nó nhắc nhở toàn bộ team kỹ thuật và phát triển sản phẩm rằng: Chúng ta không viết code để tạo ra một công cụ "theo dõi", chúng ta viết code để giải quyết "nỗi lo âu" của phụ huynh và xóa bỏ những cuộc cãi vã không đáng có trong gia đình.

---

### 3. Key Results (Kết quả then chốt) & Phân tích chuyên sâu

Để chứng minh Objective trên đã đạt được, chúng ta sẽ neo vào 3 chỉ số (Key Results) đại diện cho 3 khía cạnh cốt lõi của doanh nghiệp:

#### 🟢 KR1: Chỉ số dẫn dắt (Leading Metric - Phản ánh Hành vi)
> **Mục tiêu:** 60% yêu cầu xin tiền/hoàn ứng của sinh viên được xử lý thông qua luồng *AI Smart Request* của App thay vì nhắn tin Zalo truyền thống.

*   **Bản chất:** Đây là thước đo **Sự hình thành thói quen (Habit Formation)**.
*   **Tại sao lại quan trọng:** Sinh viên là người rất lười dùng app mới. Nếu họ vẫn dùng Zalo để xin tiền mẹ như cũ, DOMIN-H sẽ trở thành một "cái kho chết" không có dữ liệu đầu vào. Việc đạt được mốc 60% chứng minh rằng: Trải nghiệm xin tiền qua app (được AI làm đẹp hồ sơ) thực sự nhanh, mượt và ít bị từ chối hơn so với việc phải nhắn tin giải thích thủ công qua Zalo.
*   **Rủi ro nếu trượt KR này:** Chứng tỏ UX/UI của luồng Request quá rườm rà (Friction cao). Team Product sẽ phải lập tức cắt giảm các bước nhập liệu thừa để tối ưu lại.

#### 🟡 KR2: Chỉ số trễ (Lagging Metric - Phản ánh Kinh doanh)
> **Mục tiêu:** Đạt 500 phụ huynh đăng ký gói thuê bao trả phí (Subscription - Gói Học kỳ/Năm), với MRR (Doanh thu định kỳ hàng tháng) đạt tối thiểu $2,500 vào cuối quý.

*   **Bản chất:** Đây là thước đo **Sự sẵn sàng chi trả (Willingness-to-Pay / WTP)**.
*   **Tại sao lại quan trọng:** Doanh thu là câu trả lời trung thực nhất của thị trường. Nỗi đau "không biết con tiêu tiền vào đâu" có thực sự đủ lớn để phụ huynh Việt Nam chịu quẹt thẻ 99.000 VNĐ/tháng không? 500 người dùng trả phí đầu tiên (Early Adopters) chính là vé thông hành để DOMIN-H gọi vốn thành công ở vòng tiếp theo.
*   **Rủi ro nếu trượt KR này:** Nếu User dùng bản Free nhiều nhưng tỷ lệ chuyển đổi (Conversion rate) thấp, có nghĩa là chúng ta đang định giá sai (Pricing issue), hoặc rào cản cổng thanh toán (Payment gateway) quá phức tạp đối với phụ huynh lớn tuổi.

#### 🔵 KR3: Chỉ số Chất lượng (Quality Metric - Phản ánh Niềm tin)
> **Mục tiêu:** Tỷ lệ phụ huynh tiếp tục gia hạn thuê bao / tiếp tục sử dụng app (Month-2 Retention) đạt trên 75%.

*   **Bản chất:** Đây là thước đo **Mức độ hài lòng & Giá trị thực tế (Trust & Real Value)**.
*   **Tại sao lại quan trọng:** Trong tháng đầu tiên (Month 1), phụ huynh có thể mua gói trả phí vì tò mò hoặc do chốt sale tốt. Tuy nhiên, họ chỉ tiếp tục sử dụng ở tháng thứ 2 (Month 2) nếu app thực sự mang lại "Sự an tâm" và giúp gia đình bớt cãi vã. Trong ngành SaaS (Software as a Service), Retention rate $\ge 75\%$ ở tháng thứ 2 là một chỉ số cực kỳ xuất sắc.
*   **Rủi ro nếu trượt KR này:** Hiện tượng "Thùng nước thủng" (Leaky Bucket). Khách hàng vào bao nhiêu rụng bấy nhiêu. Nguyên nhân lớn nhất thường nằm ở việc sinh viên "tẩy chay" app (không chịu chụp hóa đơn nữa), dẫn đến phụ huynh thấy app vô dụng và hủy gói. Nếu Retention tụt, phải kích hoạt ngay các tính năng bảo vệ sinh viên (Private Mode) ở cột NEXT.

---
**Thông điệp cốt lõi gửi Hội đồng Đầu tư (Key Takeaway for VCs):** 
Bộ OKR này được thiết kế để không cho phép startup tự lừa dối mình bằng các chỉ số ảo. Chúng tôi đo lường việc app có thay đổi được thói quen giao tiếp (KR1) hay không, phụ huynh có chịu trả tiền (KR2) hay không, và sản phẩm có giữ được hòa khí gia đình đủ lâu để họ ở lại (KR3) hay không. Hoàn thành 3 KR này, DOMIN-H Family chính thức đạt Product-Market Fit.
