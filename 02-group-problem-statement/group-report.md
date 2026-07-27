# Group Report — Day 02

**Topic:** Hỗ trợ Onboarding nhân viên mới

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|--------------------|
| 1   | Đinh Quốc Trung    | 2A202601687 | Nhóm phó    |
| 2   | Cao Thị Thu Trang  | 2A202601885 | Nhóm trưởng |
| 3   | Trần Dương Tuấn    | 2A202601271 | Thành viên  |
| 4   | Nguyễn Doãn Hoàng  | 2A202601119 | Thành viên  |
| 5   | Phạm Hà Linh       | 2A202601041 | Thành viên  |
| 6   | Bùi Linh Đan       | 2A202601177 | Thành viên  |
| 7   | Lại Thế Rin        | 2A202601665 | Thành viên  |
| 8   | Trần Chí Tâm       | 2A202601535 | Thành viên  |
| 9   | Trương Văn Thái    | 2A202601801 | Thành viên  |
| 10  | Trương Thảo Nguyên | 2A202601389 | Thành viên  |
| 11  | Hà Hoàng Tuấn Hùng | 2A202601629 | Thành viên  |
| 12  | Bùi Thị Như Ngọc   | 2A202601882 | Thành viên  |

---

## Phase 3 — Group Convergence

### Cấu trúc nhóm lớn

Nhóm lớn gồm **12 người**, chia thành **3 nhóm nhỏ** (4 người/nhóm). Mỗi nhóm nhỏ tự scan, pitch nội bộ và chốt 1 topic đại diện. Sau đó 3 topic được trình bày trước nhóm lớn để vote chọn topic cuối cùng.

### Bước 3.1 — Kết quả 3 nhóm nhỏ

| Nhóm nhỏ | Topic đã chốt | Mô tả ngắn |
|----------|--------------|------------|
| Nhóm 1 | **Hỗ trợ Onboarding nhân viên mới** | HR mất nhiều thời gian chuẩn bị thủ công, FAQ lặp lại, new employee không có centralized hub |
| Nhóm 2 | **Catch-up Discord mỗi ngày sau giờ học** | Thành viên nhóm/lớp mất thời gian đọc lại chat Discord, catch-up thông tin sau giờ học, lặp lại 5 lần/tuần |
| Nhóm 3 | **Tóm tắt bệnh án chuẩn y khoa** | Bác sĩ / sinh viên y khoa mất thời gian đọc và tóm tắt bệnh án dài theo chuẩn y khoa |

### Bước 3.2 — Pitch + Vote nhóm lớn

| Topic | Số phiếu (trên 12 người) | Tỉ lệ |
|-------|------------------------:|:-----|
| Hỗ trợ Onboarding nhân viên mới | **7** | 58.3% |
| Catch-up Discord mỗi ngày sau giờ học | **5** | 41.7% |
| Tóm tắt bệnh án chuẩn y khoa | **0** | 0% |

**Topic được chọn:**
```
Hỗ trợ Onboarding nhân viên mới (7/12 phiếu)
```

**Vì sao thắng:**
```
- Workflow onboarding rõ ràng, nhiều actor (HR, IT, new employee, buddy), bottleneck cụ thể.
- Pain có thật: nhiều người trong nhóm từng trải qua onboarding thiếu structured.
- Impact đo được: thời gian HR, số FAQ lặp lại.
- Scope vừa phải, không quá rộng, phù hợp để đào sâu trong lab.
```

**Vì sao các topic khác không được chọn:**
```
- Catch-up Discord (5 phiếu): workflow rõ, pain thật nhưng scope hẹp hơn, giải pháp có thể chỉ là rule/workflow đơn giản,
  ít cơ hội so sánh R/W/A đa dạng.
- Tóm tắt bệnh án (0 phiếu): domain chuyên ngành y khoa, nhóm không có chuyên môn, khó validate workflow thật.
```

---

## Phase 4 — Quick Validation + Research giải pháp

### Bước 4.1 — Quick validation

#### Option A — Quick interviews / mini survey

Kết quả:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|-------|-----------------:|-------------------|-------------------|--------------------------|
| Interview HR | 2 | 2/2 xác nhận: mỗi đợt onboarding mất 3-5 ngày để chuẩn bị tài liệu và setup; 70% câu hỏi từ new employee lặp lại | 1 người nói đã dùng checklist Google Sheets | Thu hẹp: không làm toàn bộ quy trình HR, tập trung vào mảng FAQ + tài liệu tự phục vụ |
| Interview new employee | 3 | 3/3: cảm thấy choáng ngợp với lượng tài liệu, không biết bắt đầu từ đâu, hay quên bước | 1 người nói buddy tốt đã đủ | Nhấn mạnh cần centralized hub + FAQ tự động |
| Mini poll trong lớp | 8 | 6/8 từng trải qua onboarding thiếu structured; 5/8 muốn có centralized nơi tra cứu | Một số nói onboarding chỉ mất 1 ngày nếu công ty nhỏ | Tập trung vào SME/startup vừa, workflow phức tạp vừa phải |

**Insight sau validation:**
```
Pain thật không chỉ nằm ở việc "thiếu tài liệu", mà nằm ở việc tài liệu rời rạc, 
new employee không biết tìm ở đâu, và HR phải trả lời cùng một câu hỏi lặp lại nhiều lần.
Giải pháp không cần AI phức tạp — Rule (checklist, FAQ page) có thể giải quyết 60-70%.
AI có thể hỗ trợ phần trả lời câu hỏi theo ngữ cảnh và gợi ý next step.
```

### Bước 4.2 — Research giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---------------------|------|------------------------|-----------|----------------------|-------------------|
| Gusto HR Onboarding | https://gusto.com/products/hr-platform/onboarding | Tự động hóa forms, documents, task checklist | Tốt cho phần paperwork và compliance | Không hỗ trợ FAQ tự động, không personalized | Rule/checklist có thể giải quyết phần cứng; cần thêm layer hỗ trợ thông minh |
| BambooHR Onboarding | https://www.bamboohr.com/hr-software/employee-onboarding | Centralized hub cho tài liệu, tasks, e-signatures | UI tốt, task tracking rõ | Thiếu AI trả lời câu hỏi theo ngữ cảnh; giá cao cho SME | Pattern tốt: centralized hub; nhóm có thể focus vào layer AI hỗ trợ |
| Slack AI + Workflow Builder | https://slack.com/help/articles/360035563974-Guide-to-Workflow-Builder | Auto-response FAQ, workflow phê duyệt đơn giản | Tích hợp sẵn trong Slack, dễ dùng | Chỉ hoạt động trong Slack; limited customization | Workflow Builder cho thấy rule/workflow đơn giản đã giải quyết được nhiều; không cần agent ngay |
| Notion Templates (Employee Onboarding) | https://www.notion.com/templates/category/employee-onboarding | Template centralized hub, wiki, checklist | Dễ copy, dễ customize, giá rẻ | Không tự động, không AI, vẫn cần người maintain | Non-AI alternative mạnh: template đủ tốt cho 60-70% use case |

**Research takeaway:**
```
- Các giải pháp hiện tại tập trung vào phần cứng (forms, documents, task checklist).
- Khoảng trống: ít tool hỗ trợ FAQ tự động/ngữ cảnh hóa cho new employee.
- Non-AI alternative (template + checklist + FAQ page) giải quyết được phần lớn vấn đề.
- AI nên tập trung vào phần trả lời câu hỏi và gợi ý next step — phần mà rule khó làm tốt vì mỗi new employee có context khác nhau.
```

---

## Phase 5 — Workflow + Problem Statement

### Bước 5.1 — Current workflow

```
CURRENT STATE — Onboarding nhân viên mới (ước lượng 3-5 ngày preparation + 1-2 tuần ramp-up)

[HR gửi welcome email + tài liệu đính kèm: 60']
→ [IT setup account + device: 1-2 ngày chờ]  <-- bottleneck
→ [New employee đọc tài liệu rời rạc: 120']
→ [HR hướng dẫn thủ tục: 45']
→ [New employee hỏi FAQ lặp lại: 30'/lần]
→ [Buddy hướng dẫn công việc: ongoing]
→ [HR follow-up check-in: 30']
→ [New employee tự mày mò quy trình: nhiều giờ]
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|------|-------|-------|--------|-------------------|---------|
| 1 | HR | Employee info | Welcome email + tài liệu | 60 phút/đợt | Manual compose, đính kèm tài liệu rời rạc |
| 2 | IT | Request từ HR | Account, device, access | 1-2 ngày | Phụ thuộc queue IT; không tự động |
| 3 | New employee | Tài liệu từ HR | Hiểu quy trình | 120 phút | Tài liệu rời rạc, dễ overwhelmed |
| 4 | HR | Tài liệu + câu hỏi | Hướng dẫn thủ tục | 45 phút | Thông tin lặp lại mỗi đợt |
| 5 | New employee | Thắc mắc | Câu trả lời | 30 phút/lần | Cùng câu hỏi lặp lại |
| 6 | Buddy | New employee | Hướng dẫn công việc | Ongoing | Phụ thuộc buddy availability |
| 7 | HR | New employee progress | Check-in | 30 phút | Manual follow-up |

**Bottleneck chính:**
```
1. HR mất công chuẩn bị thủ công + trả lời FAQ lặp lại → tốn thời gian, dễ sót thông tin.
2. New employee overwhelmed với tài liệu rời rạc → không biết bắt đầu từ đâu.
3. Thiếu centralized hub → mỗi actor tự xoay sở, không có single source of truth.
```

### Bước 5.2 — Future workflow

```
FUTURE STATE — Onboarding nhân viên mới (ước lượng 1 ngày preparation + ramp-up giảm 40%)

[HR nhập thông tin vào hệ thống: 10']  -- Rule/form
→ [Auto-generate welcome + task checklist: 2']  -- Workflow
→ [IT auto-provision account từ trigger: 30']  -- Rule/Workflow
→ [New employee truy cập centralized hub: 5']
→ [Hub gợi ý next step + FAQ tự động: instant]  -- AI hỗ trợ FAQ
→ [New employee hỏi AI assistant thay vì HR/buddy: 2']  -- AI hỗ trợ
→ [HR check-in dashboard + exception: 15']  -- Human boundary

Fallback: AI trả lời sai → new employee tag HR/buddy vào câu hỏi cụ thể.
```

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|--------|-----:|-----------:|---------|
| Số bước thủ công (HR) | 7 | 3 | HR chỉ nhập thông tin, check-in, xử lý exception |
| Tổng thời gian HR/đợt | ~4-5 giờ | ~1-2 giờ | Giảm nhờ auto-generate + FAQ tự động |
| Số câu hỏi lặp lại new employee | ~15-20 câu/đợt | ~3-5 câu/đợt | AI FAQ handle 70-80% |
| Thời gian new employee ramp-up | ~1-2 tuần | Target giảm 30-40% | Nhờ centralized hub + next step gợi ý |
| Risk mới | Không có | AI hallucination FAQ | Cần HR review accuracy, fallback rõ |

### Bước 5.3 — Problem Statement v0

| Field | Nội dung |
|-------|---------|
| **Actor** | HR/Onboarding team (prepare + guide), new employee (learn + ask), IT (setup), buddy (mentor). Primary actor: HR và new employee. |
| **Workflow** | Mỗi đợt onboarding, HR chuẩn bị tài liệu thủ công, IT setup sau request, new employee đọc tài liệu rời rạc, hỏi FAQ lặp lại, buddy hướng dẫn, HR follow-up. |
| **Bottleneck** | (1) HR tốn 3-5 ngày preparation manual + trả lời cùng FAQ lặp lại. (2) New employee không có centralized hub, dễ overwhelmed. (3) Thiếu tự động hóa giữa các actor. |
| **Impact** | HR mất ~4-5 giờ/đợt onboarding; new employee mất ~2-3 ngày để tự mày mò; FAQ lặp lại chiếm 30% thời gian HR. Trải nghiệm onboarding kém ảnh hưởng retention. |
| **Success Metric** | (1) Giảm thời gian HR preparation từ 4-5 giờ xuống dưới 2 giờ/đợt. (2) Giảm số câu hỏi FAQ lặp lại từ 15-20 xuống dưới 5 câu/đợt. (3) New employee có thể tự tra cứu quy trình trong < 5 phút mà không cần hỏi ai. |
| **Boundary** | Không tự động gửi email hay thực hiện action thay HR; không thay thế buddy hoàn toàn; AI chỉ trả lời dựa trên tài liệu được cung cấp, không tự bịa quy trình. Scope: SME/startup vừa (20-200 nhân viên). |

---

## Phase 6 — Rule / Workflow / Agent + Decision

### Bước 6.0 — Ma trận độ phù hợp với AI

```
Bài toán của nhóm nằm ở ô: Độ phức tạp trung bình, Độ mơ hồ trung bình-thấp.

Vì sao?
- Workflow có nhiều bước (HR prepare, IT setup, new employee learn, FAQ) nhưng các bước khá rõ ràng.
- Độ mơ hồ thấp ở phần checklist, task list — có thể rule hóa.
- Độ mơ hồ cao hơn ở phần FAQ — mỗi câu hỏi có thể khác nhau, cần hiểu ngữ cảnh.
- Không cần agent vì workflow không yêu cầu tự lập kế hoạch động; các bước có thứ tự cố định.
```

### Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|-----|---------------------------|------------|--------|-------|
| **Rule** | Checklist template, FAQ page static, auto-email template | Đủ nếu new employee chỉ cần list + document | FAQ không personalized; không xử lý câu hỏi ngoài danh sách; vẫn cần HR trả lời thủ công | Không chọn làm chính, nhưng dùng cho phần checklist + auto-email |
| **Workflow** | Form HR nhập → tự động tạo checklist + centralized hub → AI FAQ + gợi ý next step → HR check-in dashboard | Hợp vì workflow tuyến tính, mỗi bước rõ input/output, AI chỉ hỗ trợ một số bước | AI FAQ sai hoặc thiếu context; new employee vẫn cần hỏi HR nếu câu hỏi ngoài scope | **Chọn** |
| **Agent** | Agent tự động chào hỏi new employee, trả lời FAQ, track progress, tự gửi reminder, tự escalate | Chỉ cần nếu new employee cần người hướng dẫn ảo 24/7 và workflow có nhiều nhánh | Quá rộng, nhiều permission, risk AI hallucination cao; new employee có thể nhận sai thông tin quan trọng | Chưa chọn |

**Mức chọn:**
```
Workflow.
```

**Vì sao chọn:**
```
- Rule không đủ: FAQ cần hiểu ngữ cảnh, không chỉ là list tĩnh.
- Workflow đủ: các bước onboarding có thứ tự rõ ràng, input/output biết trước.
- AI hỗ trợ ở phần FAQ + gợi ý next step — phần có độ mơ hồ vừa phải, lỗi không gây hậu quả nghiêm trọng (HR vẫn check).
- Human boundary rõ: HR vẫn check-in, vẫn review accuracy, vẫn xử lý exception.
```

**Vì sao không chọn mức đơn giản hơn (Rule):**
```
- FAQ không thể dùng rule tĩnh vì mỗi new employee có role, phòng ban, câu hỏi khác nhau.
- Checklist + email template giải quyết phần hành chính nhưng không giải quyết pain "không biết bắt đầu từ đâu" và "hỏi lặp lại".
```

**Vì sao không chọn mức phức tạp hơn (Agent):**
```
- Workflow không cần tự lập kế hoạch động — các bước có thứ tự cố định.
- Agent tự động action (gửi email, reminder) tạo nhiều risk và permission issues.
- Chi phí xây dựng agent cao hơn nhiều so với workflow, trong khi phần lớn giá trị đã có từ workflow + AI FAQ.
```

### Bước 6.2 — Problem Statement v1

| Field | Nội dung |
|-------|---------|
| **Actor** | HR/Onboarding team (chịu trách nhiệm chính), new employee, IT, buddy. |
| **Workflow** | HR nhập thông tin → auto-generate task checklist + centralized hub → new employee tự tra cứu + FAQ AI → HR check-in dashboard. |
| **Bottleneck** | HR tốn 4-5 giờ/đợt cho preparation manual + trả lời FAQ lặp lại; new employee không có centralized hub, mất 2-3 ngày tự mày mò. |
| **Impact** | Mỗi đợt onboarding tốn ~4-5 giờ HR + ~2-3 ngày new employee ramp-up chậm; FAQ lặp lại chiếm 30% thời gian HR. |
| **Success Metric** | (1) Giảm thời gian HR preparation từ 4-5h → <2h/đợt. (2) Giảm FAQ lặp lại từ 15-20 → <5 câu/đợt. (3) New employee tự tra cứu được quy trình trong <5 phút. |
| **Boundary** | Scope: SME 20-200 nhân viên. AI không tự động action (gửi mail, tạo account, gửi reminder). AI chỉ trả lời dựa trên tài liệu được cấp. HR review và chịu trách nhiệm accuracy. Buddy vẫn là người thật cho hướng dẫn chuyên môn. |
| **AI intervention point** | Sau khi HR nhập thông tin → AI hỗ trợ FAQ và gợi ý next step trong centralized hub. Trước khi new employee cần hỏi HR/buddy. |
| **Mức chọn** | Workflow: Rule cho checklist/auto-email + AI cho FAQ và gợi ý next step. |
| **Rủi ro & người thật kiểm tra** | Risk: AI FAQ sai/sót, new employee nhận thông tin không chính xác. Người thật kiểm tra: HR review accuracy định kỳ, new employee có thể tag HR nếu câu trả lời không rõ. |

### Bước 6.3 — Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---------|-------------------:|---------|
| Actor và workflow đã rõ chưa? | Yes | HR, new employee, IT, buddy — workflow các bước rõ |
| Baseline và success metric đã đo được chưa? | Yes | Thời gian HR, số FAQ lặp lại, thời gian new employee tự tra cứu |
| Có data/input đủ dùng chưa? | Yes | Tài liệu onboarding hiện có, FAQ log từ HR |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | HR review + fallback: new employee hỏi trực tiếp |
| Có người review/owner vận hành không? | Yes | HR là owner, check dashboard định kỳ |
| Có cách non-AI đơn giản hơn không? | Yes | Notion template + checklist + FAQ page (giải quyết ~60-70%) |

**Decision:**
```
Go với scope nhỏ (pilot).
```

**Lý do:**
```
- Problem rõ, workflow rõ, metric rõ.
- AI chỉ hỗ trợ phần FAQ + gợi ý next step — phần có risk thấp.
- Non-AI alternative (template + checklist) đã tồn tại, có thể dùng làm baseline.
- Human boundary rõ: HR review, fallback rõ.
- Scope (SME 20-200 người) vừa phải, không quá rộng.
```

**Pilot nhỏ nhất:**
```
1. Chọn 1 phòng ban và 1 đợt onboarding thật.
2. Xây centralized hub (Notion hoặc simple web page) với:
   - Checklist task tự động theo role.
   - FAQ page do HR soạn sẵn.
   - AI assistant (GPT-based) trả lời FAQ dựa trên tài liệu.
3. HR vẫn prepare manual như cũ nhưng log thời gian để so sánh.
4. Đo: thời gian HR, số FAQ new employee hỏi, thời gian new employee tự tra cứu.
5. Nếu AI trả lời sai > 20% → fallback về FAQ page tĩnh + HR manual.
```

**Exit / rollback:**
```
- Nếu AI FAQ accuracy < 80% sau 2 tuần → hạ xuống Rule: FAQ page tĩnh + checklist.
- Nếu HR vẫn mất > 3 giờ/đợt → cần review lại workflow, không phải AI.
- Nếu new employee không dùng centralized hub → cần training/communication lại.
```
