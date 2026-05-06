
# TÀI LIỆU CHIẾN LƯỢC SẢN PHẨM: DOMIN-H FAMILY
**Dự án:** Ứng dụng AI-Mediator Quản lý Tài chính Sinh viên dành cho Phụ huynh  
**Người phụ trách (Product/AI Lead):** Jimala  
**Trạng thái:** Bản nháp V1.0 (Dành cho Investor Pitch & Internal Alignment)

---

## WORKSHOP 2: LỘ TRÌNH PHÁT TRIỂN SẢN PHẨM (NOW / NEXT / LATER ROADMAP)

### 1. Triết lý xây dựng Roadmap (Roadmap Philosophy)
Đối với một sản phẩm giải quyết mâu thuẫn thế hệ (Generation Gap) như DOMIN-H Family, lộ trình phát triển không thể chỉ là một bản danh sách tính năng (Feature list). Chúng ta áp dụng framework **NOW / NEXT / LATER** để tập trung vào việc giải quyết từng lớp tâm lý của cả hai nhóm người dùng: Phụ huynh (Người trả tiền - Buyer) và Sinh viên (Người nhập liệu - End-user).

---

### 2. Bản đồ Lộ trình Tổng quan (Strategic Roadmap Overview)

| Phase | Trọng tâm Chiến lược (Strategic Focus) | Vấn đề cốt lõi cần giải quyết (Core Problem) | Key Features (Tính năng chủ đạo) |
|:---|:---|:---|:---|
| **🟢 NOW**<br>*(Q3 - Q4/2026)* | **Xóa mù dòng tiền**<br>(Transparency & Trust) | Phụ huynh mệt mỏi vì phải tự định giá khoản chi. Sinh viên báo cáo sai lệch. | 1. AI Request Summarizer<br>2. Anti-Fraud OCR |
| **🟡 NEXT**<br>*(Q1 - Q2/2027)* | **Tối ưu Cảm xúc & Giữ chân**<br>(Empathy & Retention) | Sinh viên chán nản, từ chối nhập liệu vì cảm giác bị "giám sát ngột ngạt". | 1. Private Mode (Quỹ ẩn)<br>2. AI Advocate (Đề xuất tăng hạn mức) |
| **🔵 LATER**<br>*(Tầm nhìn 2027+)* | **Tự động hóa Toàn diện**<br>(Seamless Ecosystem) | Trải nghiệm bị đứt gãy: Phụ huynh duyệt trên app nhưng phải mở app Bank để chuyển tiền. | 1. Bank/E-wallet Integration (Open Banking) |

---

### 3. Phân tích Chuyên sâu (Deep-dive Analysis)

#### 🟢 Giai đoạn NOW (MVP): Xóa mù dòng tiền & Thiết lập Quyền lực AI
*Mục tiêu: Đạt được Product-Market Fit (PMF) bằng cách chứng minh AI có thể thay thế những cuộc gọi tra khảo căng thẳng.*

*   **Vấn đề:** 80% phụ huynh hiện nay đang "chuyển khoản mù". Khi con xin tiền, họ phải tốn năng lượng để tự hỏi: "Món này mua làm gì? Giá này có bị đắt không?". Nếu tra khảo quá chi tiết, con cái sẽ gắt gỏng và dẫn đến cãi vã.
*   **Giải pháp Thực thi:**
    *   **AI Request Summarizer (Thẩm định tự động):** Biến DOMIN-H thành cổng xin tiền duy nhất. Thay vì nhắn Zalo, sinh viên dán link Shopee hoặc gửi ảnh món đồ. AI Agent lập tức cào dữ liệu, đối chiếu giá và trả về một bản "Báo cáo đề xuất giải ngân" cho phụ huynh. *Lợi ích:* Phụ huynh ra quyết định dựa trên data khách quan của AI, gạt bỏ cảm xúc cá nhân.
    *   **Anti-Fraud OCR (Trích xuất Hóa đơn siêu tốc):** Sử dụng Gemini 1.5 Flash để đọc hóa đơn ngay khi sinh viên vừa tiêu xong. Phân loại chuẩn xác dòng tiền để phụ huynh biết chính xác ngân sách sinh hoạt đang vơi đi vì hạng mục nào (Ăn uống, Học tập, hay Giải trí).

#### 🟡 Giai đoạn NEXT: Giải quyết Rủi ro Churn (Rời bỏ) từ phía Sinh viên
*Mục tiêu: Chuyển đổi trạng thái của Sinh viên từ "Bị ép dùng" sang "Tự nguyện dùng" bằng cách trao cho họ đặc quyền.*

*   **Vấn đề (Rủi ro sống còn):** Mặc dù phụ huynh là người trả tiền (Subscriber), nhưng sinh viên mới là người tạo ra dữ liệu (Data Generator). Nếu sau 2 tháng, sinh viên cảm thấy app này giống như một "vòng kim cô" hay "phần mềm gián điệp", họ sẽ viện cớ hỏng camera, mất mạng để không dùng nữa. Mất dữ liệu đồng nghĩa với việc phụ huynh sẽ hủy gói thuê bao (Churn).
*   **Giải pháp Thực thi:**
    *   **Private Mode (Chế độ Quỹ ẩn riêng tư):** Cho phép thiết lập một tỷ lệ ngân sách (VD: 15% tổng sinh hoạt phí) đưa vào "Vùng mù". AI chỉ báo cáo tổng số tiền đã tiêu trong quỹ này, tuyệt đối không liệt kê chi tiết (mua quà cho người yêu, mua đồ dùng cá nhân nhạy cảm). *Lợi ích:* Đảm bảo quyền riêng tư tối thiểu của một người trưởng thành, thể hiện sự tôn trọng của sản phẩm đối với Gen Z.
    *   **AI Advocate (Luật sư biện hộ AI):** Lập trình để AI Agent tự động ghi nhận các nỗ lực tài chính. Nếu sinh viên chi tiêu dưới hạn mức 2 tháng liên tiếp, AI sẽ chủ động gửi một Notification (Thông báo) gợi ý cho phụ huynh: *"Jimala đã quản lý tài chính rất xuất sắc trong 60 ngày qua. Đề xuất thưởng thêm 500k vào quỹ giải trí tháng này!"*. *Lợi ích:* Đưa AI trở thành "đồng minh" của sinh viên.

#### 🔵 Giai đoạn LATER: Khép kín Hệ sinh thái Giao dịch
*Mục tiêu: Trở thành Super-app Quản lý Tài chính Gia đình.*

*   **Vấn đề:** Trải nghiệm người dùng (UX) hiện tại đang bị gãy ở bước cuối cùng. Phụ huynh đọc báo cáo duyệt tiền trên DOMIN-H, nhưng sau đó phải thoát ra, mở app Vietcombank/Techcombank, copy số tài khoản, nhập số tiền để chuyển. 
*   **Giải pháp Thực thi:**
    *   **Tích hợp Open Banking API & E-wallet (MoMo/VNPay):** Kết nối trực tiếp với cổng thanh toán. Khi phụ huynh bấm nút "Duyệt" trên báo cáo của AI, ứng dụng sẽ tự động kích hoạt luồng chuyển tiền (Deep link) hoặc trừ thẳng vào ví điện tử đã liên kết.
*   **Lý do đặt ở LATER:** Việc tích hợp API ngân hàng yêu cầu hệ thống bảo mật cấp độ cao (PCI DSS), giải quyết các rào cản pháp lý khắt khe và chi phí duy trì server lớn. Ở giai đoạn Seed/MVP, việc dồn nguồn lực vào luồng này là quá rủi ro. Chỉ thực hiện khi đã chứng minh được mô hình kinh doanh và gọi vốn thành công ở Series A.

---
**Thông điệp cốt lõi gửi Hội đồng Đầu tư (Key Takeaway):** 
Roadmap của DOMIN-H Family không bị "say" tính năng công nghệ. Mỗi tính năng được đặt vào timeline đều phục vụ một mục đích kinh doanh rõ ràng: **NOW** để thu hút dòng tiền trả phí đầu tiên, **NEXT** để bảo vệ chỉ số Retention (Giữ chân), và **LATER** để mở rộng quy mô (Scale).
