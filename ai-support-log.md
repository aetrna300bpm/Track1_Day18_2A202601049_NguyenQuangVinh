# AI Support Log — Day 18
## Nguyễn Quang Vinh · MHV `2A202601049` · Nhóm 2 · Case B — AI Notes

Lab cho phép dùng AI để gợi ý cơ chế, tạo dữ liệu mẫu, canned output, code và rà soát câu hỏi dẫn dắt; **không** cho phép dùng AI để tạo quote/observation/feedback không tồn tại, làm sạch evidence đến mức mất ranh giới giữa lời user và diễn giải, hay viết hộ phần đóng góp và reflection cá nhân. Log này khai báo đúng những gì đã dùng.

---

## 1. AI đã hỗ trợ những gì

**Đọc và tổng hợp đầu vào**

* Đọc 10 file PDF hướng dẫn Day 18 và slide guide (`data.js`) để rút ra 6 chặng, 5 gate và danh sách anti-pattern.
* Đọc lại repo Day 17 của nhóm (`README.md`, `interview/notes.md`) và ánh xạ từng quote của NV-01 / NV-02 vào bảng Evidence Snapshot.

**Chặng 1–3 — thiết kế**

* Soạn bản nháp Hypothesis Problem theo cấu trúc `situation / user / job / barrier / consequence`, và bảng "Điều vẫn chưa được chứng minh".
* Dựng lại Solution Parking Lot 6 hướng từ hành vi đã quan sát ở Day 17 (nhóm không lưu Parking Lot thành file ở Day 17).
* Đề xuất trục so sánh `USER CREATES → CO-CREATE → AI CREATES` và ba điểm A/B/C trên trục đó; soạn Comparison Contract, Distance check và Human–AI Decision Table.

**Chặng 4 — build**

* Viết toàn bộ code ba prototype (`index.html`, `option-a/b/c.html`): HTML/CSS/JS tự chứa, không CDN, không lưu trữ trình duyệt.
* Tạo **content fixture giả lập** dùng chung: bài học *Vector Database & RAG cơ bản*, 3 slide và 3 câu giảng viên nói thêm ngoài slide. Đây là **nội dung dựng sẵn cho prototype**, không phải dữ liệu từ user thật.
* Tạo **canned AI output**: 4 thẻ gợi ý của Option B và bản nháp 7 khối của Option C, trong đó cố ý cài **một khối AI suy diễn quá đà** (ngưỡng "10.000 tài liệu") để test xem tester có kiểm tra badge uncertainty không.
* Chạy Playwright kiểm thử ba luồng và chụp màn hình từng bước.

**Chặng 5–6 — chuẩn bị test**

* Soạn Test Prompt, Observation Focus 5 điểm, luật facilitation và bảng counterbalance thứ tự A/B/C cho ba tester.
* Soạn **template rỗng** cho Feedback Note và Group Synthesis.

---

## 2. Điểm sai / hời hợt của AI và cách đã sửa

| # | AI làm sai hoặc hời hợt | Đã sửa thế nào |
| :-- | :--- | :--- |
| 1 | Mặc định bài lab chạy theo cấu trúc **3 người / 3 option / 3 tester** như tài liệu, trong khi nhóm chỉ có 2 người. | Phải hỏi lại và chốt cách chia: một người phụ trách chính 2 option + 2 phiên test, người kia 1 option + 1 phiên, để vẫn đủ **ba Feedback Notes** cho Gate 5 thay vì hạ xuống 2. |
| 2 | Giả định repo Day 17 đã có sẵn **Solution Parking Lot** vì Chặng 2 yêu cầu "mở lại pool ≥5 hướng". Kiểm tra thì repo không có. | Không bịa ra một Parking Lot "đã có từ Day 17". Dựng lại công khai từ hành vi trong hai practice note, và ghi rõ trong Design Sheet rằng đây là bản **tái tạo**. |
| 3 | Bản nháp đầu của ba option nghiêng về mô tả **màn hình** (bản A đẹp hơn, bản C nhiều thông tin hơn) — đúng anti-pattern *"3 options chỉ khác màu sắc, wording hoặc bố cục"*. | Ép lại theo trục agency: chốt **AI Act / Ask / Don't Act** trước, rồi mới thiết kế màn hình từ quyết định đó. Khóa 70% context, content và component cho cả ba. |
| 4 | Option C ban đầu chỉ có bản nháp "đúng và đẹp" — không có gì để tester phát hiện AI sai, nên không test được Human control. | Cài một khối AI **suy diễn quá đà** có nhãn vàng và dòng cơ sở nói rõ *"ngưỡng 10.000 tài liệu KHÔNG có trong bài học — AI tự thêm vào"*. |
| 5 | Code Option B để hiệu ứng xuất hiện chạy lại cho **mọi** thẻ ở mỗi lần re-render → cả rail nhấp nháy, tester dễ mất dấu thẻ mới. | Phát hiện qua ảnh chụp Playwright. Bỏ animation, thay bằng nhãn tĩnh **MỚI** trên thẻ của mốc hiện tại. |
| 6 | AI **không thể** và **không được** tạo Feedback Note. | Ba phiên test chưa chạy tại thời điểm chuẩn bị tài liệu. `prototype-feedback-note.md` và `group-feedback-synthesis.md` được để **trống có cấu trúc**, kèm cảnh báo ở đầu file. Mọi observation và quote sẽ do người facilitate ghi từ phiên thật. |

---

## 3. Ranh giới evidence — khai báo rõ

| Loại nội dung | Nguồn |
| :--- | :--- |
| Quote của NV-01, NV-02 trong Evidence Snapshot | **Người thật**, từ 2 phỏng vấn ghi âm ngày 17/08/2026 của Day 17 |
| Cột "Điều nhóm đang diễn giải" | **Diễn giải của nhóm**, tách riêng khỏi cột lời user |
| Bài học *Vector Database & RAG*, slide, lời giảng | **Nội dung dựng sẵn cho prototype** — không phải bài học có thật, không phải dữ liệu user |
| Gợi ý của Option B, bản nháp của Option C | **Canned output**, viết tay sẵn — không gọi model |
| Feedback Notes, Group Synthesis | **Chưa có.** Chỉ được điền từ phiên test thật |

---

## 4. Phần tự viết — Nguyễn Quang Vinh

> Điền bằng lời của chính mình sau khi đã chạy phiên test. Đây là phần lab yêu cầu phải là phản ánh cá nhân, không được để AI viết hộ.

**Chỗ tôi thấy AI hiểu sai bối cảnh nhóm mình nhất:**
> ……………………………………………………………………………………

**Điều tôi tự quyết định khác với đề xuất của AI, và vì sao:**
> ……………………………………………………………………………………

**Sau khi test thật, điều gì trong thiết kế ba option hóa ra là AI (và tôi) đoán sai:**
> ……………………………………………………………………………………
