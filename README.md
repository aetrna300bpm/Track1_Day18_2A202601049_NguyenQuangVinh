# Track 1 — Day 18: Multiple Prototypes & Human–AI Design
## Case B — AI Notes: Personal Learning Notes

---

## 📋 1. Thông tin cá nhân và nhóm

* **Mã học viên (MHV):** `2A202601411`
* **Họ và tên:** Trần Thị Vân Anh (Case B Lead)
* **Tên nhóm:** Nhóm 2 — Track 1 VLearn AI Product Building
* **Thành viên nhóm:**
  1. Trần Thị Vân Anh (MHV `2A202601411`) — Case B Lead
  2. Nguyễn Quang Vinh (MHV `2A202601049`) — Member
* **Case:** **Case B — AI Notes: Personal Learning Notes** *(tiếp tục đúng case của Day 17, không đổi case)*
* **Đầu vào từ Day 17:** [Track1_Day17_2A202601049_NguyenQuangVinh](https://github.com/aetrna300bpm/Track1_Day17_2A202601049_NguyenQuangVinh)

> ### ⚠️ Nhóm 2 người — khai báo trước những chỗ thiếu so với chuẩn
>
> Bài lab thiết kế cho nhóm **3 người**. Nhóm 2 có **2 người**. Nhóm chọn khai báo thẳng thay vì bù cho đủ số:
>
> | | Chuẩn của lab | Nhóm 2 | Xử lý |
> | :--- | :--- | :--- | :--- |
> | Solution Options | 3 | **3** ✅ | Giữ đủ để Gate 2 không bị hạ chuẩn |
> | Practice Notes (Day 17) | 3 | **2** | Nhóm chỉ phỏng vấn 2 người. Giữ con số thật |
> | Feedback Notes (Day 18) | 3 | **2** | Mỗi thành viên facilitate 1 phiên với 1 tester ngoài nhóm |
>
> Ảnh hưởng cụ thể của việc thiếu phiên thứ ba được nêu ở [`group-feedback-synthesis.md` §4](group-feedback-synthesis.md#4-hạn-chế-của-chính-đợt-test-này), không giấu đi.

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

**Điều chưa được chứng minh — và trạng thái sau khi test Day 18**

| # | Điều chưa chứng minh (chốt ở Chặng 1) | Sau 2 phiên test |
| :-- | :--- | :--- |
| 1 | Học viên chịu bỏ bao nhiêu thao tác trong lúc nghe giảng | 🔽 Họ muốn thao tác ít nhất có thể, để giữ được mạch nghe giảng |
| 2 | Có tin & dùng lại ghi chú AI tự viết mà mình không đánh dấu | 🔽 Cả hai đều không tin và không thấy hữu ích |
| 3 | "Đủ" của một bản ghi chú là keyword hay tóm tắt đầy đủ | 🔽 **Đảo hướng giả định của nhóm** — ghi chú không phải bản tóm tắt |
| 4 | 2 practice interview chưa phải validation | ⏸️ Vẫn nguyên |

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
| **Trade-off** | Không ghi thừa — nhưng quên đánh dấu là mất luôn | Không bỏ sót — nhưng cắt luồng học | Tốn 0 thao tác — nhưng AI quyết định hộ |
| **Prototype** | [`prototype/option-a.html`](prototype/option-a.html) | [`prototype/option-b.html`](prototype/option-b.html) | [`prototype/option-c.html`](prototype/option-c.html) |

**Hub cho tester (bắt đầu ở đây):** [`prototype/index.html`](prototype/index.html) — link đầy đủ trong [`prototype-link.md`](prototype-link.md)

**Distance check**

* **A khác B vì** A chỉ dựng từ những gì user đã tự tay đánh dấu và AI đứng im tới khi được gọi; B để AI chủ động phát hiện ứng viên **trong lúc** học rồi hỏi user duyệt từng cái.
* **B khác C vì** B chia quyết định thành nhiều lượt nhỏ trong lúc học và không viết gì nếu user không duyệt; C dồn toàn bộ quyết định vào **một lần review bản nháp đã viết sẵn** sau bài học.
* **A khác C vì** A không suy diễn ngoài vùng user đánh dấu; C tự chọn nội dung nào quan trọng cho cả bài — nên hậu quả khi AI sai ở C lớn hơn hẳn.

Human–AI Decision Table đầy đủ: [`three-option-design-sheet.md` §3](three-option-design-sheet.md#chặng-3--humanai-decision-table)

### ✨ Phương án D — bản gộp A+B, dựng sau khi test

Đây là **Next Change đã được dựng thành prototype**, không phải option thứ tư mang đi so sánh. Nó ra đời **sau** và **nhờ** hai phiên test.

```
BÔI ĐEN (trong lúc học)  →  AI IM LẶNG  →  CUỐI BÀI: USER GỌI  →  AI MỞ RỘNG (tách riêng)
```

| Quyết định | Đến từ bằng chứng nào |
| :--- | :--- |
| Đánh dấu bằng **bôi đen**, không phải bấm-vào-dòng | `T1` không phát hiện ra chữ trong slide bấm được; `T1` tự đề xuất bôi đen |
| AI **im lặng hoàn toàn** trong lúc học | `T1`: *"cúi xuống đọc cái ngẩng lên là không hiểu gì rồi"* — chi phí thật là mất mạch nghe giảng |
| AI chỉ **mở rộng đoạn đã đánh dấu**, và chỉ khi được bấm | `T1` và `T2` độc lập cùng muốn AI ở vai trò *làm rõ cái tôi đã chọn*, không phải *chọn hộ* |
| Phần AI nằm **thu gọn dưới** chữ của user, có nhãn *"không phải chữ của bạn"* | Cả hai chọn A vì tự chủ; `T1`: *"ghi chú nhằm personalize"* |
| Recovery là **bỏ**, không phải **sửa** | Ở B và C không ai dùng nút *Sửa* — họ thà tự gõ lại |

**Prototype:** [`prototype-v2/index.html`](prototype-v2/index.html) · Thiết kế đầy đủ: [`three-option-design-sheet.md` §6](three-option-design-sheet.md#chặng-6--sau-khi-test--phương-án-d)

> Phương án D **chưa được test với ai**. Giả thuyết trung tâm của nó — *bôi đen dễ khám phá hơn bấm-vào-dòng* — vẫn chưa có bằng chứng.

---

## 🙋 4. Đóng góp của các thành viên trong nhóm

Nhóm gồm **2 thành viên**, công việc được phân chia cân bằng **50 / 50** xuyên suốt các chặng của dự án:

### 👩‍💻 Trần Thị Vân Anh — MHV `2A202601411` (Case B Lead)

| Hạng mục | Phần Vân Anh phụ trách |
| :--- | :--- |
| **Option chịu trách nhiệm chính** | **Option B — Live suggestion rail** *(Cơ chế AI Ask thời gian thực trong lúc học)* |
| **Xây dựng giải pháp & Human–AI** | Đề xuất cơ chế duyệt từng thẻ gợi ý; chủ trì biên soạn bài toán Hypothesis Problem và xây dựng Human–AI Decision Table |
| **Evidence & Phỏng vấn** | Interviewer của **NV-01** ở Day 17; đưa trích dẫn quote NV-01 và phân tích rào cản thao tác vào Evidence Snapshot |
| **Deploy & Hạ tầng** | Deploy 3 prototype & trang Hub lên Netlify ([`chipper-basbousa-bccf28.netlify.app`](https://chipper-basbousa-bccf28.netlify.app/prototype/)), tạo môi trường truy cập live cho tester |
| **Facilitation & Feedback** | Facilitate **Phiên 2 (Tester 2)**; trực tiếp ghi chép quan sát và lập tài liệu [`prototype-feedback-note-vananh.md`](prototype-feedback-note-vananh.md) |
| **Đồng tổng hợp bài học** | Phối hợp tổng hợp kết quả 2 phiên test, rút ra bài học Next Change và đồng thiết kế **Phương án D** |

---

### 👨‍💻 Nguyễn Quang Vinh — MHV `2A202601049` (Member)

| Hạng mục | Phần Vinh phụ trách |
| :--- | :--- |
| **Option chịu trách nhiệm chính** | **Option A — Marker-first** và **Option C — Auto recap** *(Cơ chế AI Don't Act & AI Act)* |
| **Shared context / content** | Dựng content fixture dùng chung: bài học *Vector Database & RAG cơ bản*, 3 slide và 3 câu giảng viên nói thêm; khóa Comparison Contract |
| **Shared visual components** | Header, player mock, panel phải, bảng màu, chip nguồn và reset path (`Bắt đầu lại` / `Tất cả phương án`) dùng chung cho A/B/C |
| **Evidence & Phỏng vấn** | Interviewer của **NV-02** ở Day 17; đưa quote NV-02 vào Evidence Snapshot và phân tích workflow thực tế |
| **Chuẩn bị test** | Soạn Test Prompt, Observation Focus 5 điểm, luật facilitation, bảng counterbalance thứ tự A/B/C ([`test-script.md`](test-script.md)) |
| **Facilitation & Feedback** | Facilitate **Phiên 1 (Tester 1)**; trực tiếp lập tài liệu [`prototype-feedback-note.md`](prototype-feedback-note.md) |
| **Đồng tổng hợp bài học** | Phối hợp tổng hợp Group Feedback Synthesis và lập trình giao diện bản gộp **Phương án D** ([`prototype-v2/`](prototype-v2/index.html)) |

---

## 🧪 5. Prototype Feedback

**Hai phiên, hai tester ngoài nhóm, hai thứ tự chạy ngược nhau.** Cả hai tester đều có relevant context (đang học online và tự ghi chú: một người dùng Notepad, một người viết ra vở).

| Phiên | Facilitator | Tester | Thứ tự | Note |
| :--- | :--- | :--- | :--- | :--- |
| F1 | Nguyễn Quang Vinh | `T1` | A → B → C | [`prototype-feedback-note.md`](prototype-feedback-note.md) |
| F2 | Trần Thị Vân Anh | `T2` | B → C → A | [`prototype-feedback-note-vananh.md`](prototype-feedback-note-vananh.md) |

### Bốn pattern trùng nhau ở cả hai phiên

1. **Cả hai chọn Option A**, ở hai thứ tự chạy ngược nhau — nên không phải hiệu ứng thứ tự.
2. **Affordance đánh dấu của A vô hình.** `T1`: *"Em không biết là bấm được vào chữ trong slide để ghi note đấy."* `T2`: khó hiểu tương tác đánh dấu.
3. **Cơ chế duyệt-từng-thẻ của B bị hiểu ngược bởi cả hai người** — họ tưởng thẻ đã tự nằm trong ghi chú. Và chi phí thật không phải số lần bấm: `T1` — *"cúi xuống đọc cái ngẩng lên là không hiểu gì rồi."*
4. **C bị bác ở mức khái niệm, không phải mức giao diện.** `T1`: *"chẳng liên quan gì đến ghi chú, out of scope… ghi chú nhằm personalize còn cái này thì viết hết hộ."* `T2`: *"note cái gì vậy, cho vào AI tóm tắt cho nhanh."*

Phát hiện số 4 phủ định một giả định nằm dưới cả ba option: nhóm coi **ghi chú = bản tóm tắt bài học**. Với cả hai tester, **ghi chú = ghi lại thứ mình thấy quan trọng hoặc chưa hiểu, để review sau**.

### Next Change

> Ghép Option A và Option B: giữ *người dùng tự đánh dấu* làm cơ chế chính, đổi thao tác sang **bôi đen**, và để **AI mở rộng đúng những đoạn đã đánh dấu — chỉ khi người dùng bấm yêu cầu, ở cuối bài**. Bỏ cơ chế AI tự chọn nội dung của Option C.

Đã dựng thành [`prototype-v2/`](prototype-v2/index.html).

### Still Unproven

* Điều gì làm việc ghi chú hữu ích **với số đông** — hai tester có hai phong cách ghi chú khác nhau.
* **Bôi đen có dễ khám phá hơn bấm-vào-dòng hay không — chưa test.**
* **Toàn bộ phần thiết kế evidence & uncertainty chưa được kiểm chứng.** Không phiên nào đo được tester có đọc chip nguồn hay badge *"AI suy ra"* không — đây là lỗi thiết kế phương pháp của nhóm.
* **Thiếu phiên thứ ba.** Mọi "pattern" ở trên thực chất là "hai trên hai".
* Facilitator phiên 1 tự nhận **có mớm lời** cho tester lúc họ đang im lặng suy nghĩ.

**Câu nhóm kết luận:** *"Với Hypothesis Problem này, chúng tôi đã thử ba cách giải. Hai tester ngoài nhóm, chạy ở hai thứ tự khác nhau, đều chọn cách giải do người dùng tự đánh dấu và đều bác cách giải AI tự viết bản nháp ở mức khái niệm. Vì vậy iteration tiếp theo chúng tôi giữ cơ chế đánh dấu của A, đổi thao tác sang bôi đen, và chuyển AI từ vai trò chọn-nội-dung sang vai trò mở-rộng-theo-yêu-cầu."*

**Câu nhóm không kết luận:** ~~*"User đã xác nhận solution này đúng."*~~

Tổng hợp đầy đủ: [`group-feedback-synthesis.md`](group-feedback-synthesis.md)

---

## 🤖 6. AI Support Log

Bản đầy đủ: [`ai-support-log.md`](ai-support-log.md)

* **AI đã giúp:** đọc và tổng hợp tài liệu lab + repo Day 17; soạn nháp Hypothesis Problem, Parking Lot, Comparison Contract và Human–AI Decision Table; viết toàn bộ code bốn prototype HTML tự chứa; tạo content fixture và canned output; soạn Test Prompt và sheet ghi chép; biên tập field notes viết tay thành Feedback Note có cấu trúc; chạy Playwright kiểm thử.
* **AI sai / hời hợt ở đâu:** **làm hộ luôn phần brainstorm** — đưa ra trọn bộ ba ý tưởng prototype thay vì để nhóm tự nghĩ, trong khi mục tiêu của bài là rèn brainstorm; mặc định cấu trúc nhóm 3 người; giả định Day 17 đã có Parking Lot; bản nháp đầu ba option nghiêng về khác **màn hình** thay vì khác **cơ chế**; Option C ban đầu không có chỗ nào cho tester phát hiện AI sai; và **hai bug thật trong code AI viết** — biến `open` / `status` trùng tên với `document.open` / `window.status` làm nút *Thu gọn* và *Xoá hết* im lặng không hoạt động.
* **Tôi tự sửa gì:** hỏi off-script trong lúc phỏng vấn thay vì bám bộ câu hỏi soạn sẵn — chính từ đó mới ra đề xuất ghép A và B; chốt lại cách chia việc cho nhóm 2 người; ép thiết kế lại theo trục `Act / Ask / Don't Act` trước khi vẽ màn hình.
* **Điều tôi và AI cùng đoán sai:** ghi chú **không** nhằm tóm tắt đầy đủ nội dung buổi học. Với nhiều người, ghi chú là ghi lại những gì quan trọng / khó hiểu / đặc biệt. Cả ba option đều dựng trên giả định sai này.
* **Ranh giới AI không được vượt:** mọi observation và quote trong repo **chỉ đến từ hai phiên test thật**. Chỗ facilitator không quan sát được thì ghi là *không quan sát được* — không suy đoán ngược từ hành vi.

---

## 📁 Cấu trúc repo

```
Track1_Day18_2A202601049_NguyenQuangVinh/
├── README.md                            # File này
├── three-option-design-sheet.md         # Chặng 1–4 + §6 thiết kế Phương án D
├── prototype-link.md                    # Link A/B/C và Phương án D
├── test-script.md                       # Chặng 5: Test Prompt + Observation Focus
├── prototype-feedback-note.md           # Phiên 1 — Vinh facilitate, tester T1
├── prototype-feedback-note-vananh.md    # Phiên 2 — Vân Anh facilitate, tester T2
├── group-feedback-synthesis.md          # Tổng hợp 2 phiên + Next Change + Still Unproven
├── ai-support-log.md                    # Khai báo dùng AI + reflection cá nhân
├── prototype/                           # BẢN ĐÃ TEST — không sửa sau feedback
│   ├── index.html                       # Hub — tester bắt đầu ở đây
│   ├── option-a.html
│   ├── option-b.html
│   └── option-c.html
└── prototype-v2/                        # Next Change — chưa test
    └── index.html                       # Phương án D — bản gộp A+B
```

---

## ✅ Đối chiếu năm Gate

| Gate | Trạng thái | Ở đâu |
| :--- | :--- | :--- |
| **1 — Evidence Continuity** | ✅ | Hypothesis Problem đủ 5 thành phần, nối tới quote NV-01/NV-02, có 4 điều chưa chứng minh và trạng thái sau test — mục 2 |
| **2 — Meaningful Options** | ✅ | Comparison Contract khoá user/situation/task/outcome/content; khác biệt ở cơ chế và phân quyền user–AI; màn hình bối cảnh giống hệt nhau ở cả ba — Design Sheet §2 |
| **3 — Human Control** | ✅ thiết kế · ⚠️ chưa kiểm chứng | Human–AI Decision Table đủ 5 hàng cho A/B/C/D; mỗi option ≥2 đường recovery thao tác được. **Nhưng hai phiên test không đo được hành vi đọc evidence** — nhóm ghi rõ thay vì tuyên bố đã chứng minh |
| **4 — Test-ready** | ✅ | Hai tester ngoài nhóm tự chạy hết A/B/C. Facilitator phiên 1 và phiên 2 đều xác nhận **không phải giải thích hộ** |
| **5 — Learning, not Praise** | ⚠️ **2 Feedback Notes, không phải 3** | Có pattern và khác biệt giữa hai người, một Next Change đã dựng thành prototype, và Still Unproven nêu rõ. Nhóm **không** tuyên bố solution đã validated. Thiếu phiên thứ ba được khai báo ở mục 1 và `group-feedback-synthesis.md` §4 |
