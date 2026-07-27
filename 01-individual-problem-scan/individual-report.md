Case: **Xử lý ticket hỗ trợ CSKH**

Nhân vật ví dụ: Linda, Customer support (CSKH) tại một sàn E-commerce, mỗi ngày phải xử lý từ 40-50 tickets từ khách hàng. Nhiệm vụ của Linda là phải phân loại, trả lời hoặc escalate cho đúng team (Vận hành, Kho, Kế toán). 

## Vì sao đây là ví dụ tốt?

- Có actor cụ thể.
- Có workflow lặp lại hằng ngày.
- Có bottleneck rõ.
- Có thể so sánh Rule / Workflow / Agent.
- Có thể vẽ before/after workflow.

# 01 — Individual Problem Scan

## Scan rộng

Minh scan 10 problems, vượt mức tối thiểu 5.

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi ticket phải đọc, phân loại category rồi mới xử lý | Nhân viên CSKH | ~40-50 ticket/ngày, 1-2 phút/ticket chỉ để phân loại |
| 2 | Lặp lại | Trả lời các câu hỏi lặp đi lặp lại bằng tay dù nội dung gần giống nhau | Nhân viên CSKH, khách hàng | Khoảng 30% ticket là câu hỏi lặp lại |
| 3 | Tốn thời gian | Tra cứu thông tin đơn hàng ở nhiều hệ thống trước khi trả lời | Nhân viên CSKH | 3-5 phút/ticket để tra cứu chéo |
| 4 | Tốn thời gian | Escalate ticket sai bộ phận, phải chuyển tay lại nhiều lần | Nhân viên CSKH, bộ phận tiếp nhận | Mất thêm 1 vòng chuyển tiếp/ticket bị escalate sai |
| 5 | AI có thể tốt hơn | Không có gợi ý câu trả lời mẫu theo ngữ cảnh ticket | Nhân viên mới | Nhân viên mới trả lời chậm hơn nhân viên cũ |
| 6 | AI có thể tốt hơn | Không phát hiện được ticket khẩn cấp để ưu tiên xử lý trước | Khách hàng, nhân viên CSKH | Một số ticket khẩn cấp bị xử lý trễ do xếp hàng theo thứ tự đến |
| 7 | Pain từ người khác | Khách hàng phải hỏi lại nhiều lần vì câu trả lời đầu không đủ thông tin | Khách hàng, nhân viên CSKH | Trung bình 1.5 lượt hỏi lại/ticket |
| 8 | Pain từ người khác | Ticket escalate thiếu thông tin làm phiền bộ phận tiếp nhận | Bộ phận tiếp nhận, nhân viên CSKH | Bộ phận tiếp nhận phải hỏi lại để bổ sung context |
| 9 | Tốn thời gian | Tổng hợp báo cáo cuối ngày về ticket đã xử lý | Trưởng nhóm | 20-30 phút/ngày |
| 10 | Lặp lại | Viết note bàn giao ca cho ca sau | Nhân viên CSKH | 10-15 phút/ca |

Vì sao phần scan này mạnh:

- Có scan rộng trước khi hội tụ.
- Có nhiều lăng kính khác nhau.
- Mỗi problem có actor và dấu hiệu thật.
- Không bắt đầu bằng "làm chatbot" hoặc "xây agent".

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Phân loại + tra cứu chéo thông tin ticket (#1, #3) | Lặp lại cao nhất, có metric thời gian rõ, ảnh hưởng trực tiếp tốc độ phản hồi | Độ chính xác phân loại tự động cần đạt bao nhiêu mới đủ tin dùng |
| 2 | Gợi ý câu trả lời mẫu theo ngữ cảnh (#5) | Giảm gánh nặng cho nhân viên mới, có thể đo bằng thời gian phản hồi | Cần kho câu trả lời mẫu chất lượng làm input |
| 3 | Phát hiện ticket khẩn cấp để ưu tiên (#6) | Impact cao (giữ khách), nhưng khó đo baseline | Định nghĩa "khẩn cấp" chưa rõ ràng, dễ gây tranh cãi |

## Problem Card #1 — Phân loại & tra cứu chéo thông tin ticket

**Problem 1 câu:**  
Mỗi ticket nhân viên CSKH mất 4-7 phút chỉ để phân loại và tra cứu chéo thông tin đơn hàng ở nhiều hệ thống trước khi trả lời.

**Actor:**  
Nhân viên CSKH xử lý ticket hằng ngày trên hệ thống hỗ trợ (Zendesk).

**Thời điểm / bối cảnh:**  
Diễn ra liên tục trong ca làm việc, đặc biệt cao điểm vào giờ hành chính khi lượng ticket dồn về nhiều.

**Current workflow:**
```text
1. Đọc ticket
2. Xác định category (giao hàng/hoàn tiền/lỗi kỹ thuật...)
3. Tra hệ thống kho/thanh toán để lấy thông tin đơn hàng
4. Soạn câu trả lời
5. Gửi
6. Đóng hoặc escalate ticket
```

**Bottleneck:**  
Bước 2-3 (phân loại + tra cứu chéo) — 4-7 phút/ticket, lặp lại 40-50 lần/ngày.

**Impact:**  
Khoảng 3-4 tiếng/ngày/nhân viên chỉ dành cho bước phân loại + tra cứu, chiếm phần lớn thời gian ca làm việc.

**Success metric:**  
Giảm thời gian phân loại + tra cứu xuống dưới 2 phút/ticket, không tăng tỷ lệ escalate sai.

**Non-AI alternative:**  
Checklist phân loại cố định + link tra cứu nhanh — giảm phần nào nhưng không tự động hoá được việc gom dữ liệu từ nhiều hệ thống.

**AI hypothesis:**  
AI tự động phân loại category + tự động pull thông tin đơn hàng liên quan từ các hệ thống, nhân viên chỉ cần review và trả lời.

**Quick gut:**  
Workflow.

### Draft current workflow
```text
CURRENT STATE — 6-9 phút/ticket
[1 Đọc ticket: 1']
→ [2 Phân loại category: 2']
→ [3 Tra cứu chéo hệ thống: 3-5']  <-- bottleneck
→ [4 Soạn câu trả lời: 2-3']
→ [5 Gửi: 0.5']
→ [6 Đóng/escalate: 0.5']
```

### Draft future workflow
```text
FUTURE STATE — 3-4 phút/ticket
[1 AI tự phân loại + pull thông tin đơn hàng: 0.5']
→ [2 Nhân viên review dữ liệu đã gom: 1']  <-- human boundary
→ [3 Soạn câu trả lời (có gợi ý sẵn): 1-1.5']
→ [4 Gửi/đóng: 0.5']

Fallback: AI phân loại sai/thiếu dữ liệu → nhân viên tự tra cứu như cũ.
```

---

## Problem Card #2 — Gợi ý câu trả lời mẫu theo ngữ cảnh

**Problem 1 câu:**  
Nhân viên mới phải tự soạn câu trả lời từ đầu cho từng ticket vì không có gợi ý mẫu theo ngữ cảnh, khiến thời gian phản hồi chậm hơn đáng kể so với nhân viên cũ.

**Actor:**  
Nhân viên CSKH mới (trong giai đoạn onboarding, chưa tích lũy đủ kinh nghiệm xử lý các loại ticket phổ biến).

**Thời điểm / bối cảnh:**  
Diễn ra liên tục trong ca làm việc, rõ nhất trong 1-2 tháng đầu sau khi nhân viên mới vào làm.

**Current workflow:**
```text
1. Đọc nội dung ticket
2. Tự nhớ/tìm lại cách xử lý case tương tự (hỏi đồng nghiệp hoặc lục tài liệu cũ)
3. Soạn câu trả lời từ đầu
4. Kiểm tra lại thông tin trước khi gửi
5. Gửi phản hồi cho khách hàng
```

**Bottleneck:**  
Bước 2-3 — không có sẵn câu trả lời mẫu theo ngữ cảnh, nhân viên mới mất nhiều thời gian dò lại cách xử lý và tự soạn.

**Impact:**  
Nhân viên mới trả lời chậm hơn nhân viên cũ; kéo theo tăng thời gian chờ của khách hàng và tăng khối lượng hỏi lại đồng nghiệp trong team.

**Success metric:**  
Rút ngắn khoảng cách thời gian phản hồi giữa nhân viên mới và nhân viên cũ trong 2-4 tuần đầu onboarding.

**Non-AI alternative:**  
Xây dựng thư viện mẫu câu trả lời (FAQ nội bộ) theo category — giảm phần nào nhưng cần cập nhật thủ công liên tục và không tự khớp ngữ cảnh ticket cụ thể.

**AI hypothesis:**  
AI đọc nội dung ticket, tự gợi ý câu trả lời mẫu phù hợp ngữ cảnh; nhân viên chỉnh sửa trước khi gửi.

**Quick gut:**  
Workflow.

### Draft current workflow
```text
CURRENT STATE — 5-8 phút/ticket
[1 Đọc ticket: 0.5']
→ [2 Dò cách xử lý tương tự: 2-3']  <-- bottleneck
→ [3 Soạn câu trả lời từ đầu: 2-3']
→ [4 Kiểm tra lại: 0.5']
→ [5 Gửi: 0.5']
```

### Draft future workflow
```text
FUTURE STATE — 2-3 phút/ticket
[1 Đọc ticket: 0.5']
→ [2 AI gợi ý câu trả lời mẫu theo ngữ cảnh: 0.5']
→ [3 Nhân viên chỉnh sửa cho phù hợp: 1-1.5']  <-- human boundary
→ [4 Gửi: 0.5']

Fallback: Gợi ý AI không phù hợp → nhân viên tự soạn như cũ.
```

---

## Problem Card #3 — Phát hiện ticket khẩn cấp để ưu tiên xử lý

**Problem 1 câu:**  
Ticket từ khách hàng đang bức xúc hoặc muốn huỷ đơn bị xử lý theo thứ tự đến trước thay vì được ưu tiên (nhân viên CSKH vẫn xử lý thủ công theo thứ tự), khiến tình huống dễ trở nên nghiêm trọng hơn trước khi được xử lý.

**Actor:**  
Khách hàng có ticket mang tính khẩn cấp (giận dữ, đe dọa huỷ đơn) và nhân viên CSKH tiếp nhận ticket đó.

**Thời điểm / bối cảnh:**  
Xảy ra bất kỳ lúc nào trong ca làm việc, đặc biệt ở khung giờ cao điểm khi lượng ticket dồn nhiều.

**Current workflow:**
```text
1. Ticket vào hàng đợi theo thứ tự thời gian gửi
2. Nhân viên xử lý tuần tự theo thứ tự đó
3. Ticket khẩn cấp chỉ được nhận diện khi nhân viên đọc đến
4. Xử lý sau khi đã phát hiện tính khẩn cấp
```

**Bottleneck:**  
Bước 1-3 — không có cơ chế nhận diện mức độ khẩn cấp trước khi ticket được đọc, nên ticket khẩn cấp có thể nằm chờ như ticket thường.

**Impact:**  
Một số ticket khẩn cấp bị xử lý trễ, làm khách hàng bức xúc hơn; tăng rủi ro mất khách hàng hoặc nhận đánh giá tiêu cực công khai.

**Success metric:**  
Giảm thời gian phản hồi trung bình cho ticket khẩn cấp xuống mức ưu tiên hàng đầu (VD: dưới 5 phút thay vì chờ theo thứ tự), không tăng thời gian xử lý ticket thường.

**Non-AI alternative:**  
Đặt từ khóa cảnh báo thủ công (VD: "huỷ đơn", "khiếu nại") để lọc — giảm phần nào nhưng dễ bỏ sót các cách diễn đạt khác không nằm trong danh sách từ khóa cố định.

**AI hypothesis:**  
AI phân tích nội dung/giọng điệu ticket ngay khi vào hệ thống, tự gắn nhãn mức độ khẩn cấp và đẩy lên đầu hàng đợi; nhân viên vẫn là người xử lý cuối cùng.

**Quick gut:**  
Workflow.

### Draft current workflow
```text
CURRENT STATE — không giới hạn thời gian chờ
[1 Ticket vào hàng đợi theo thời gian gửi]
→ [2 Xử lý tuần tự]  <-- bottleneck
→ [3 Phát hiện khẩn cấp khi đọc đến]
→ [4 Xử lý ưu tiên (đã trễ)]
```

### Draft future workflow
```text
FUTURE STATE — ưu tiên tức thời
[1 AI phân tích + gắn nhãn khẩn cấp ngay khi ticket vào: tức thời]
→ [2 Ticket khẩn cấp tự động lên đầu hàng đợi]
→ [3 Nhân viên xử lý ticket khẩn cấp trước]  <-- human boundary
→ [4 Ticket thường xử lý theo thứ tự còn lại]

Fallback: AI gắn nhãn sai → nhân viên có thể tự đánh dấu lại mức độ ưu tiên.
```