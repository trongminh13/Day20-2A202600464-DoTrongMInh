# TÀI LIỆU CHIẾN LƯỢC SẢN PHẨM: DOMIN-H FAMILY
**Dự án:** Ứng dụng AI-Mediator Quản lý Tài chính Sinh viên dành cho Phụ huynh  
**Người phụ trách (Product/AI Lead):** Jimala  
**Trạng thái:** Bản nháp V1.0 (Dành cho Investor Pitch & Internal Alignment)

---

## WORKSHOP 1: ĐÁNH GIÁ RICE & MA TRẬN ƯU TIÊN TÍNH NĂNG (FEATURE PRIORITIZATION)

### 1. Bối cảnh Bài toán (Problem Context)
Trong mô hình gia đình Việt Nam, phụ huynh là người chu cấp nguồn vốn (trung bình 4-8 triệu VNĐ/tháng), nhưng lại thiếu công cụ kiểm soát dòng tiền sau khi giải ngân. Việc kiểm tra thủ công (gọi điện, nhắn tin tra khảo) thường tạo ra "đứt gãy giao tiếp" (Communication Breakdown) – sinh viên cảm thấy bị xâm phạm quyền riêng tư và có xu hướng nói dối, trong khi phụ huynh rơi vào trạng thái lo âu vì mất kiểm soát.

**Giải pháp (The Solution):** Đưa AI Agent vào vai trò "Người phán xử" (Mediator). AI đứng giữa để thẩm định tính hợp lý của các khoản chi, tự động báo cáo cho phụ huynh và bảo vệ sự tự tôn của sinh viên. 

---

### 2. Định nghĩa 5 Tính năng MVP Cốt lõi (Core Feature Definition)

Trước khi chấm điểm, chúng ta cần định nghĩa rõ phạm vi kỹ thuật của 5 tính năng đang được đưa lên bàn cân:

1. **Smart Request & AI Approval (Luồng xin tiền thông minh):** 
   - *Flow:* Sinh viên dán link sản phẩm (Shopee, web) hoặc chụp ảnh món đồ cần mua. AI tự động cào dữ liệu (web scraping) để đối chiếu giá thị trường, đánh giá mức độ thiết yếu và tạo một bản tóm tắt xin tiền gửi thẳng đến màn hình của phụ huynh. Bố mẹ chỉ cần bấm "Duyệt".

2. **AI Receipt Audit (Kiểm toán Hóa đơn bằng OCR):** 
   - *Flow:* Ứng dụng trực tiếp model Gemini 1.5 Flash để xử lý hình ảnh hóa đơn siêu tốc. Trích xuất các trường dữ liệu (Tên món, Tổng tiền, Ngày giờ) và phân loại danh mục. Bao gồm cơ chế phát hiện chỉnh sửa số liệu (Anti-fraud) hoặc thời gian phi logic.

3. **Red Flag Alerts (Cảnh báo Rủi ro Tự động):** 
   - *Flow:* Hệ thống thiết lập các ngưỡng cảnh báo (Threshold). Nếu phát hiện dòng tiền đổ vào các danh mục nhạy cảm (Game nạp thẻ, Bar/Pub) hoặc tần suất mua sắm xa xỉ tăng vọt, AI sẽ bắn Push Notification khẩn cấp cho phụ huynh.

4. **AI Parenting Coach (Trợ lý Giao tiếp Gia đình):** 
   - *Flow:* Phân tích biểu đồ chi tiêu hàng tuần, sau đó tạo ra các kịch bản hội thoại (Prompt suggestions) giúp bố mẹ nhắn tin khuyên nhủ con cái một cách tinh tế, sử dụng ngôn ngữ của Gen Z thay vì giọng điệu ra lệnh.

5. **Family Task & Reward (Nhiệm vụ & Phần thưởng):** 
   - *Flow:* Gamification. Phụ huynh thiết lập KPIs (đạt GPA 3.5, tham gia workshop VinAI, lấy chứng chỉ IELTS) để tự động mở khóa thêm hạn mức tiền tiêu vặt cho tháng sau.

---

### 3. Phân tích & Chấm điểm RICE (RICE Scoring Matrix)

*Công thức: Score = (Reach × Impact × Confidence) / Effort*  
*(Giả định tập user mục tiêu trong quý Launch là 3,000 phụ huynh tại các cụm đại học mật độ cao như khu vực Thanh Xuân).*

| ID | Tên Tính năng | Reach (Q1) | Impact (0.25-3) | Confidence | Effort (PM) | **RICE Score** |
|:---|:---|:---:|:---:|:---:|:---:|:---:|
| **F1** | Smart Request & AI Approval | 2,000 | 3 *(Massive)* | 90% | 3 | **1,800** |
| **F2** | AI Receipt Audit (OCR) | 2,000 | 3 *(Massive)* | 80% | 4 | **1,200** |
| **F3** | Red Flag Alerts | 1,500 | 3 *(Massive)* | 70% | 2 | **1,575** |
| **F4** | AI Parenting Coach | 1,000 | 2 *(High)* | 60% | 3 | **400** |
| **F5** | Family Task & Reward | 800 | 1.5 *(Medium)* | 50% | 3 | **200** |

#### 3.1. Luận giải chi tiết (Rationale Deep-dive):

*   **Về Smart Request (F1 - Điểm cao nhất):** Đây là mỏ neo giữ chân người dùng (Retention Hook). Sinh viên có động lực sử dụng vì nó là kênh giải ngân nhanh nhất. Với phụ huynh, Impact đạt mức tối đa (3) vì giải quyết trực tiếp khoảnh khắc "Rút ví". Confidence đạt 90% do API web scraping và tóm tắt văn bản hiện tại hoạt động cực kỳ ổn định.
*   **Về AI Receipt Audit (F2):** Reach và Impact đều ở mức tuyệt đối. Tuy nhiên, Confidence bị kéo xuống 80% và Effort đẩy lên 4 Person-Months (PM). Lý do: Xử lý hóa đơn rách, mờ, in nhiệt tại các quán ăn vỉa hè Việt Nam là một bài toán hóc búa, đòi hỏi nhiều nỗ lực tinh chỉnh (fine-tuning) model nhận diện hình ảnh và xây dựng luồng Fallback UX (Human-in-the-loop).
*   **Về Red Flag Alerts (F3):** Reach chỉ 1,500 vì không phải sinh viên nào cũng kích hoạt ngưỡng rủi ro. Nhưng Effort cực thấp (2 PM) do chỉ cần viết các hàm logic cảnh báo dựa trên dữ liệu đã phân loại từ F1 và F2.
*   **Về Parenting Coach & Task Reward (F4, F5):** Confidence rất thấp do văn hóa gia đình Việt phức tạp, AI khó xử lý mượt mà ngay giai đoạn đầu. Mô hình Task/Reward khiến app mang cảm giác "quản lý trẻ cấp 1", dễ gây tác dụng ngược với nhóm sinh viên.

---

### 4. Ma trận Ưu tiên 2x2 (Value vs. Effort Matrix) & Chiến lược Thực thi

Dựa vào điểm RICE (đại diện cho Value) và thời gian thực thi (Effort), chúng ta phân bổ 5 tính năng này vào ma trận để quyết định Scope cho phiên bản MVP.

#### 🚀 4.1. QUICK WINS (Giá trị cao - Nỗ lực thấp) → Làm ngay lập tức
*   **[F3] Red Flag Alerts:** 
    *   *Chiến lược:* Xây dựng hệ thống cảnh báo sớm. Đây là tính năng dễ truyền thông (Marketing) nhất. Phụ huynh sẵn sàng trả tiền thuê bao (Subscription) chỉ để "Mua sự an tâm", đảm bảo có người canh gác dòng tiền khỏi các cạm bẫy xã hội.

#### 🎯 4.2. STRATEGIC BETS (Giá trị cao - Nỗ lực cao) → Lõi công nghệ (Moat)
*   **[F1] Smart Request & [F2] AI Receipt Audit:** 
    *   *Chiến lược:* Đây là "Hào cản kinh tế" (Moat) giúp DOMIN-H Family đánh bại mọi đối thủ làm app quản lý chi tiêu truyền thống. Phải chấp nhận đổ nguồn lực kỹ thuật (7 Person-Months) để làm luồng AI mượt mà nhất. Chúng ta đang không bán phần mềm, chúng ta đang bán một "Thẩm định viên AI" làm việc 24/7 cho gia đình.

#### 🗑️ 4.3. NON-STARTERS (Giá trị thấp - Nỗ lực cao) → Loại bỏ khỏi MVP
*   **[F4] AI Parenting Coach & [F5] Family Task & Reward:** 
    *   *Chiến lược:* Gạch bỏ thẳng tay khỏi Sprint hiện tại. Ở giai đoạn Seed, nguồn lực là hữu hạn. Việc tập trung vào giao diện Task/Reward sẽ làm loãng định vị sản phẩm và lãng phí thời gian của team Frontend/Backend. Sẽ xem xét lại ở Phase 2 (Năm 2027) khi đã có đủ Data hành vi.

---
**Kết luận cho Investor:** Kế hoạch thực thi (Execution Plan) trong 8 tuần tới của dự án sẽ dồn 100% tài nguyên kỹ thuật để hoàn thiện cụm **Smart Request - Receipt Audit - Red Flag**. Đây là công thức đảm bảo Product-Market Fit nhanh nhất với tệp phụ huynh Việt Nam.
