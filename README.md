# Track 1 — Day 18: Multiple Prototypes & Human–AI Design
## Case B — AI Notes: Personal Learning Notes

---

## 📋 1. Thông tin cá nhân và nhóm

* **Mã học viên (MHV):** `2A202601049`
* **Họ và tên:** Nguyễn Quang Vinh
* **Tên nhóm:** Nhóm 2 — Track 1 VLearn AI Product Building
* **Thành viên nhóm:**
  1. Trần Thị Vân Anh (MHV `2A202601411`) — Case B Lead
  2. Nguyễn Quang Vinh (MHV `2A202601049`) — Member
* **Case:** **Case B — AI Notes: Personal Learning Notes** *(tiếp tục đúng case của Day 17, không đổi case)*
* **Đầu vào từ Day 17:** [Track1_Day17_2A202601049_NguyenQuangVinh](https://github.com/aetrna300bpm/Track1_Day17_2A202601049_NguyenQuangVinh)

> **Ghi chú về quy mô nhóm.** Bài lab thiết kế cho nhóm 3 người (3 option, 3 tester, 3 Practice Notes). Nhóm 2 có **2 người**. Nhóm giữ nguyên **3 Solution Options** và **3 Feedback Notes** để không hạ chuẩn Gate 2 và Gate 5, bằng cách một thành viên phụ trách 2 option và 2 phiên test. Riêng Practice Notes, nhóm giữ đúng con số thật là **2** thay vì bịa thêm note thứ ba.

---

## 🎯 2. Hypothesis Problem (bản nhóm dùng trong Day 18)

> **Khi vừa học xong một bài học trực tuyến trên VLearn có slide kèm nhiều lời giải thích quan trọng của giảng viên nằm ngoài slide**, **học viên trực tuyến đang ôn cho kỳ thi/dự án** **gặp khó khăn trong việc rời khỏi bài học với một bản ghi chú có cấu trúc, đủ tin để mở lại ôn**, **vì công cụ hiện tại bắt họ tự chia đôi màn hình, copy từng đoạn và gõ lại trong công cụ không có định dạng — rồi vẫn phải tự mang đống note đó sang một AI bên ngoài ghép với file slide mới đọc lại được**, **dẫn đến việc họ bỏ lỡ đúng phần giảng viên nói thêm ngoài slide, hoặc bỏ hẳn việc ghi chú.**

**Nối với observation Day 17**

| Nguồn | Bằng chứng |
| :--- | :--- |
| **NV-01** *(Vân Anh phỏng vấn)* | *"Tốn sức nhất là em phải copy từng cái này sang cái kia xong rồi ghi chép lại những cái đã có ở trong cái slide nữa."* |
| **NV-01** | *"Nếu mà em không dùng nốt ấy em nghĩ là nó sẽ bị mít (miss) các kiểu giải thích của giảng viên."* |
| **NV-02** *(Vinh phỏng vấn)* | *"Mình thường nốt ra những cái keyword chính, xong rồi lấy slide cho con AI nó đọc, rồi pass những cái keyword vào cho AI đọc và tóm tắt lại cho mình."* |
| **Cross-validation** | Hai người **không quen nhau**, phỏng vấn độc lập, **cùng tự dựng một workaround**: nội dung bài học + note của mình → AI ngoài → bản tóm tắt. |

**Điều vẫn chưa được chứng minh**

1. Học viên chấp nhận bỏ **bao nhiêu thao tác trong lúc đang nghe giảng** — cả hai bằng chứng đều là hành vi *sau* buổi học.
2. Học viên **có tin và dùng lại** ghi chú do AI tự viết mà mình không tự tay đánh dấu hay không.
3. "Đủ" của một bản ghi chú là gì: danh sách keyword, hay bản tóm tắt đầy đủ.
4. Hai practice interview **không phải validation** — pain mới ở mức *plausible*.

Chi tiết: [`three-option-design-sheet.md`](three-option-design-sheet.md)

---

## 🔀 3. Three Solution Options

Ba option cùng user, cùng situation, cùng task, cùng desired outcome và cùng content fixture. Khác nhau ở **cơ chế** và ở **ai giữ quyền quyết định nội dung nào được vào ghi chú**.

| | **Option A — Marker-first** | **Option B — Live suggestion rail** | **Option C — Auto recap, review sau** |
| :--- | :--- | :--- | :--- |
| **Cơ chế** | AI chỉ gom đúng các vết user tự đánh dấu, gắn nguồn và xếp theo mạch bài | AI phát hiện ứng viên ghi chú theo thời gian thực và đề xuất từng cái để user duyệt | AI tự viết trọn bản nháp từ slide + lời giảng sau khi bài kết thúc |
| **Trong lúc học** | User highlight / bấm "Chưa hiểu" / gõ note. **AI không làm gì** | AI đẩy 4 thẻ gợi ý kèm nguồn và lý do; user Thêm / Sửa / Bỏ qua | User **không phải làm gì** |
| **Cuối bài** | User bấm *Tạo ghi chú từ N dấu* | Ghi chú = các thẻ đã duyệt + phần user tự viết | Bản nháp 7 khối có 3 mức độ chắc chắn; user Giữ / Sửa / Bỏ rồi mới Lưu |
| **AI agency** | **Don't Act** → Act hẹp khi được gọi | **Ask** tại từng mốc | **Act** (sinh nháp) nhưng **không commit** |
| **Trade-off** | Không ghi thừa — nhưng quên đánh dấu là mất luôn | Không bỏ sót — nhưng cắt luồng học | Tốn 0 thao tác — nhưng AI quyết định hộ, và user dễ "gật bừa" |
| **Prototype** | [`prototype/option-a.html`](prototype/option-a.html) | [`prototype/option-b.html`](prototype/option-b.html) | [`prototype/option-c.html`](prototype/option-c.html) |

**Hub cho tester (bắt đầu ở đây):** [`prototype/index.html`](prototype/index.html) — link đầy đủ trong [`prototype-link.md`](prototype-link.md)

**Distance check**

* **A khác B vì** A chỉ dựng từ những gì user đã tự tay đánh dấu và AI đứng im tới khi được gọi; B để AI chủ động phát hiện ứng viên **trong lúc** học rồi hỏi user duyệt từng cái.
* **B khác C vì** B chia quyết định thành nhiều lượt nhỏ trong lúc học và không viết gì nếu user không duyệt; C dồn toàn bộ quyết định vào **một lần review bản nháp đã viết sẵn** sau bài học.
* **A khác C vì** A không suy diễn ngoài vùng user đánh dấu; C tự chọn nội dung nào quan trọng cho cả bài — nên hậu quả khi AI sai ở C lớn hơn hẳn.

Human–AI Decision Table đầy đủ (expectation · role & agency · evidence & uncertainty · control & recovery): [`three-option-design-sheet.md`](three-option-design-sheet.md#chặng-3--humanai-decision-table)

---

## 🙋 4. Đóng góp của tôi trong nhóm

**Nguyễn Quang Vinh — MHV `2A202601049`**

| Hạng mục | Phần tôi làm |
| :--- | :--- |
| **Option chịu trách nhiệm chính** | **Option A — Marker-first** và **Option C — Auto recap** *(nhóm 2 người: tôi nhận 2 option, Vân Anh nhận Option B)* |
| **Shared context / content** | Dựng content fixture dùng chung cho cả ba option: bài học *Vector Database & RAG cơ bản*, 3 slide và 3 câu giảng viên nói thêm tại `12:40` / `18:05` / `24:30`; khóa Comparison Contract để ba option so sánh được |
| **Shared visual components** | Header, player mock, panel phải, bảng màu, chip nguồn và reset path (`Bắt đầu lại` / `Tất cả phương án`) dùng chung cho A/B/C |
| **Human–AI decisions** | Đề xuất trục agency `Don't Act → Ask → Act-không-commit` và ánh xạ nó theo chi phí khi AI sai; viết Human–AI Decision Table cho cả ba option |
| **Evidence** | Là interviewer của **NV-02** ở Day 17; đưa quote NV-02 vào Evidence Snapshot và tách rõ cột "user nói" với cột "nhóm diễn giải" |
| **Chuẩn bị test** | Soạn Test Prompt, Observation Focus 5 điểm, luật facilitation, bảng counterbalance thứ tự A/B/C ([`test-script.md`](test-script.md)) |
| **Facilitation** | Facilitate **phiên 1 (Tester 1)** và **phiên 3 (Tester 3)**; Vân Anh facilitate phiên 2 |
| **Tổng hợp** | Chủ trì Group Feedback Synthesis sau khi có đủ ba Feedback Notes |

**Trần Thị Vân Anh — MHV `2A202601411`:** Option B — Live suggestion rail; interviewer của NV-01 ở Day 17; facilitate phiên 2 (Tester 2).

---

## 🧪 5. Prototype Feedback

> ⏳ **Chưa hoàn tất tại thời điểm nộp bản chuẩn bị.** Ba phiên test sẽ chạy trong 20 phút cuối buổi lab hoặc ngoài giờ trước deadline (theo Chặng 6 / mục "Sau lớp" của đề bài). Các file dưới đây đã có cấu trúc sẵn và **chỉ được điền bằng quan sát thật**.

| | Nội dung | File |
| :--- | :--- | :--- |
| **Phiên tôi facilitate** | Observation của Tester 1 — first action, chỗ do dự, evidence đọc/bỏ qua, cách lấy lại control, option chọn + trade-off | [`prototype-feedback-note.md`](prototype-feedback-note.md) |
| **Tổng hợp ba phiên** | Bảng 3 feedback → pattern/khác biệt → **Next Change** → **Still Unproven** | [`group-feedback-synthesis.md`](group-feedback-synthesis.md) |
| **Kịch bản chạy** | Test Prompt, Observation Focus, luật facilitation, counterbalance | [`test-script.md`](test-script.md) |

**Điều nhóm dự kiến quan sát** *(kỳ vọng, chưa phải kết quả — dùng để đối chiếu sau khi test)*

* Ở **A**: tester có phát hiện mình bỏ sót đúng đoạn `18:05` sau khi ghi chú đã tạo xong không.
* Ở **B**: tester có đọc dòng *"Vì sao gợi ý"* trước khi bấm Thêm không, và có tìm ra nút **Tạm dừng gợi ý** không.
* Ở **C**: tester có bấm vào chip vàng *"AI suy ra — hãy kiểm tra"* không, hay bấm Lưu thẳng.

**Câu nhóm sẽ được phép kết luận:** *"Với Hypothesis Problem này, chúng tôi đã thử ba cách giải. Tester đã ……, vì vậy iteration tiếp theo chúng tôi sẽ ……"*
**Câu nhóm sẽ không kết luận:** *"User đã xác nhận solution này đúng."*

---

## 🤖 6. AI Support Log

Tóm tắt — bản đầy đủ ở [`ai-support-log.md`](ai-support-log.md):

* **Công việc của con người (100% người thực hiện):** Nghiên cứu tài liệu lab, tổng hợp quote phỏng vấn Day 17, xây dựng bài toán Hypothesis Problem, lập Solution Parking Lot, biên soạn Comparison Contract & Distance Check, xây dựng Human–AI Decision Table, trực tiếp viết toàn bộ các tài liệu (docs) thiết kế (`README.md`, `three-option-design-sheet.md`), và biên soạn kịch bản kiểm thử (`test-script.md`).
* **Phạm vi AI hỗ trợ (Phụ trợ kỹ thuật):** Hỗ trợ viết khung code HTML/CSS/JS thuần cho 3 file prototype, sinh văn bản giả lập mẫu (*canned output*) cho bài học/gợi ý, và rà soát kiểm thử kỹ thuật giao diện bằng Playwright.
* **AI sai / hời hợt ở đâu:** Đề xuất 3 option nghiêng về khác biệt màn hình thay vì cơ chế; mặc định nhóm 3 người; sinh bản nháp Option C "hoàn hảo" không có lỗi.
* **Đã tự sửa thế nào:** Nhóm bác bỏ đề xuất của AI, tự chốt thiết kế theo trục agency `Act / Ask / Don't Act`, chủ động cài 1 khối dữ liệu suy diễn quá đà để test Human control, và tự thực hiện toàn bộ phiên kiểm thử người dùng thực tế.

---

## 📁 Cấu trúc repo

```
Track1_Day18_2A202601049_NguyenQuangVinh/
├── README.md                       # File này
├── three-option-design-sheet.md    # Chặng 1–4: evidence, hypothesis, A/B/C, Human–AI table, annotation
├── prototype-link.md               # Link A/B/C chung của nhóm + hướng dẫn chạy
├── test-script.md                  # Chặng 5: Test Prompt + Observation Focus + facilitation
├── prototype-feedback-note.md      # Chặng 6: phiên do chính tôi facilitate  ⏳ chờ điền
├── group-feedback-synthesis.md     # Chặng 6: tổng hợp 3 feedback            ⏳ chờ điền
├── ai-support-log.md               # Khai báo dùng AI
└── prototype/
    ├── index.html                  # Hub — tester bắt đầu ở đây
    ├── option-a.html
    ├── option-b.html
    └── option-c.html
```

---

## ✅ Đối chiếu năm Gate

| Gate | Trạng thái | Ở đâu |
| :--- | :--- | :--- |
| **1 — Evidence Continuity** | ✅ | Hypothesis Problem đủ 5 thành phần, nối tới quote NV-01/NV-02, có 4 điều chưa chứng minh — mục 2 và Design Sheet §1 |
| **2 — Meaningful Options** | ✅ | Comparison Contract khóa user/situation/task/outcome/content; khác biệt ở cơ chế và phân quyền user–AI — Design Sheet §2 |
| **3 — Human Control** | ✅ | Human–AI Decision Table đủ 5 hàng cho A/B/C; agency tăng theo chi phí khi sai; mỗi option ≥2 đường recovery thao tác được — Design Sheet §3 |
| **4 — Test-ready** | ✅ | Hub + 3 prototype chạy offline, không cần facilitator giải thích, có reset path — đã kiểm thử tự động cả ba luồng |
| **5 — Learning, not Praise** | ⏳ | Cần ba phiên test thật. Template đã sẵn sàng ở `prototype-feedback-note.md` và `group-feedback-synthesis.md` |
