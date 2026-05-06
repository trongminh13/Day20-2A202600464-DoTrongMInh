
# TÀI LIỆU CHIẾN LƯỢC SẢN PHẨM: DOMIN-H FAMILY
**Dự án:** Ứng dụng AI-Mediator Quản lý Tài chính Sinh viên dành cho Phụ huynh  
**Người phụ trách (Product/AI Lead):** Jimala  
**Trạng thái:** Bản nháp V1.0 (Dành cho Investor Pitch & Internal Alignment)

---

## WORKSHOP 4: BẢN ĐỒ RỦI RO & PHƯƠNG ÁN DỰ PHÒNG (DEPENDENCY MAP & MITIGATION PLAN)

### 1. Triết lý Quản trị Rủi ro
DOMIN-H Family hoạt động với một mô hình rủi ro đặc thù: **Người trả tiền (Phụ huynh) KHÔNG PHẢI là Người tạo ra dữ liệu (Sinh viên)**. Sự lệch pha về động lực (Incentive misalignment) này, cộng với những giới hạn của công nghệ OCR hiện tại tại thị trường Việt Nam, tạo ra 3 điểm nghẽn tử huyệt (Single points of failure). Dưới đây là cách chúng ta cô lập và hóa giải chúng.

---

### 2. Dependency #1: Nút thắt Người dùng (Sinh viên tẩy chay App) - 🔴 RỦI RO SỐNG CÒN

*   **Bối cảnh (Context):** Để app hoạt động, sinh viên phải chủ động dùng app để xin tiền và chụp hóa đơn.
*   **Kịch bản tồi tệ nhất (Worst-case Scenario):** Sinh viên cảm thấy app này là một "phần mềm gián điệp" tước đoạt tự do của họ. Họ có phản ứng chống đối tiêu cực bằng cách: cố tình chụp ảnh mờ, báo lỗi app, hoặc đơn giản là kiên quyết đòi bố mẹ chuyển tiền qua Zalo như cũ. 
*   **Hậu quả:** App không có Data đầu vào. Phụ huynh thấy app vô dụng -> Hủy gói thuê bao (Churn rate 100%).
*   **Plan B (Mitigation Strategy):**
    *   **Tái định vị AI (AI Repositioning):** Ngay từ màn hình Onboarding của sinh viên, AI phải xưng hô như một "Trợ lý bảo vệ quyền lợi" chứ không phải "Camera giám sát".
    *   **Tung vũ khí "Private Mode" (Quỹ Ẩn):** Thiết lập ngay một vùng không gian an toàn (Safe Zone) chiếm khoảng 10-15% tổng ngân sách. Với ngân sách này, AI tuyệt đối không quét chi tiết, chỉ báo cáo tổng chi. 
    *   **Quyền kháng cáo (Right to Appeal):** Trước khi báo cáo gửi về máy bố mẹ, sinh viên luôn có quyền xem trước (Preview) và đính kèm lời giải thích nếu thấy khoản chi đó dễ gây hiểu lầm.

---

### 3. Dependency #2: Nút thắt Công nghệ (Độ chính xác của OCR trên hóa đơn Việt Nam) - 🟡 RỦI RO CHẤT LƯỢNG

*   **Bối cảnh (Context):** Model Gemini 1.5 Flash rất mạnh, nhưng thực tế thị trường bán lẻ/F&B Việt Nam (đặc biệt là các quán cơm sinh viên, tạp hóa) sử dụng giấy in nhiệt chất lượng kém, hoặc thậm chí chỉ viết tay lên giấy nháp.
*   **Kịch bản tồi tệ nhất (Worst-case Scenario):** AI đọc sai số tiền (từ 50.000đ thành 500.000đ) hoặc phân loại sai (từ "Mua sách" thành "Giải trí/Bar"). Phụ huynh đọc báo cáo -> Tức giận gọi điện mắng mỏ con cái. Sinh viên bị oan -> Mất niềm tin hoàn toàn vào sự công bằng của DOMIN-H.
*   **Plan B (Mitigation Strategy):**
    *   **Thiết lập Ngưỡng an toàn (Confidence Threshold):** Nếu điểm tự tin của mô hình AI đối với bức ảnh đó thấp hơn 75% (`confidence_score < 0.75`), hệ thống **tuyệt đối không** tự động ghi nhận vào báo cáo của phụ huynh.
    *   **Human-in-the-loop (Con người can thiệp):** AI sẽ tạo một thông báo đẩy (Push notification) về máy sinh viên: *"Jimala ơi, hóa đơn này hơi mờ, AI không chắc lắm. Có phải bạn vừa chi 50.000đ cho Ăn uống không? Bấm Xác nhận giúp AI nhé!"*.
    *   **Cứu cánh bằng Voice Note:** Cho phép sinh viên dùng tính năng "Ghi âm" (Speech-to-text) để khai báo các khoản chi vỉa hè không hề có hóa đơn.

---

### 4. Dependency #3: Nút thắt Kinh doanh (Friction tại Cổng thanh toán) - 🟡 RỦI RO DOANH THU

*   **Bối cảnh (Context):** Startup SaaS (Software-as-a-Service) thường sống bằng mô hình MRR (Doanh thu định kỳ hàng tháng) thông qua việc tự động trừ tiền thẻ tín dụng (Visa/Mastercard Auto-renew).
*   **Kịch bản tồi tệ nhất (Worst-case Scenario):** Phụ huynh (45-55 tuổi) tại Việt Nam rất e ngại việc add thẻ Visa vào một app lạ để trừ tiền tự động. Họ bỏ ngang ở màn hình thanh toán. Chúng ta có User, có Impact, nhưng trượt hoàn toàn mục tiêu Doanh thu (KR2).
*   **Plan B (Mitigation Strategy):**
    *   **Thiết kế lại Gói cước (Repackaging):** Chuyển từ việc ép "Trả phí hàng tháng" sang mô hình "Bán đứt theo chu kỳ". Đẩy mạnh gói **Học kỳ (6 tháng)** hoặc **Năm học (12 tháng)**. Phụ huynh rất quen với tư duy "Đóng học phí 1 cục từ đầu năm" cho con.
    *   **Địa phương hóa Cổng thanh toán:** Loại bỏ rào cản thẻ Visa. Tích hợp trực tiếp **QR Code VNPay / MoMo / Napas**. Phụ huynh chỉ cần dùng app Banking mở lên quét mã trong 5 giây là xong.
    *   **Gia hạn thủ công qua Zalo ZNS:** Thay vì tự động trừ tiền âm thầm gây phản cảm, khi gần hết hạn gói cước, AI Agent sẽ gửi một tin nhắn Zalo chăm sóc khách hàng cực kỳ tinh tế kèm link thanh toán gia hạn.

---
**Tổng kết Gửi Nhà đầu tư (Executive Takeaway):** 
Chúng tôi hiểu rõ rằng công nghệ AI chỉ giải quyết được 50% bài toán, 50% còn lại là tâm lý hành vi con người và thói quen bản địa. Bản đồ rủi ro này đảm bảo DOMIN-H Family không bị "mù" trước các biến số rủi ro tại thị trường Việt Nam. Chúng tôi đã có sẵn bộ giảm xóc (Mitigation) ở cả 3 mặt trận: Trải nghiệm Sinh viên, Chất lượng Mô hình AI, và Kênh thu tiền Phụ huynh.
