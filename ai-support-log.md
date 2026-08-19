# AI Support Log — Day 18
## Nguyễn Quang Vinh · MHV `2A202601049` · Nhóm 2 · Case B — AI Notes

Lab cho phép dùng AI để gợi ý cơ chế, tạo dữ liệu mẫu, canned output, code và rà soát câu hỏi dẫn dắt; **không** cho phép dùng AI để tạo quote/observation/feedback không tồn tại, làm sạch evidence đến mức mất ranh giới giữa lời user và diễn giải, hay viết hộ phần đóng góp và reflection cá nhân. Log này khai báo đúng những gì đã dùng.

---

## 1. AI đã hỗ trợ những gì

**Đọc và tổng hợp đầu vào**

* Đọc 10 file PDF hướng dẫn Day 18 và slide guide để rút ra 6 chặng, 5 gate và danh sách anti-pattern.
* Đọc lại repo Day 17 của nhóm và ánh xạ từng quote của NV-01 / NV-02 vào bảng Evidence Snapshot.

**Chặng 1–3 — thiết kế**

* Soạn bản nháp Hypothesis Problem theo cấu trúc `situation / user / job / barrier / consequence`, và bảng "Điều vẫn chưa được chứng minh".
* Dựng lại Solution Parking Lot 6 hướng từ hành vi đã quan sát ở Day 17 (Day 17 nhóm không lưu Parking Lot thành file).
* Đề xuất trục so sánh `USER CREATES → CO-CREATE → AI CREATES` và ba điểm A/B/C trên trục đó; soạn Comparison Contract, Distance check và Human–AI Decision Table.

**Chặng 4 — build**

* Viết toàn bộ code bốn prototype (`prototype/index.html`, `option-a/b/c.html`, `prototype-v2/index.html`): HTML/CSS/JS tự chứa, không CDN, không lưu trữ trình duyệt.
* Tạo **content fixture giả lập** dùng chung: bài học *Vector Database & RAG cơ bản*, 3 slide và 3 câu giảng viên nói thêm ngoài slide. Đây là **nội dung dựng sẵn cho prototype**, không phải dữ liệu từ user thật.
* Tạo **canned AI output**: 4 thẻ gợi ý của Option B, bản nháp 7 khối của Option C, và 12 đoạn mở rộng của Phương án D — trong đó cố ý cài các chỗ AI vượt ra ngoài nội dung bài học để test xem tester có kiểm tra không.
* Chạy Playwright kiểm thử toàn bộ luồng của cả bốn prototype và chụp màn hình từng bước.

**Chặng 5–6 — chuẩn bị và tổng hợp**

* Soạn Test Prompt, Observation Focus 5 điểm, luật facilitation và bảng đảo thứ tự A/B/C.
* Soạn sheet ghi chép field notes cho hai phiên.
* **Sau khi nhận field notes viết tay của hai facilitator**: biên tập thành Feedback Note có cấu trúc, dựng bảng Group Synthesis, và dựng Phương án D từ Next Change do nhóm chốt.

---

## 2. Điểm sai / hời hợt của AI và cách đã sửa

| # | AI làm sai hoặc hời hợt | Đã sửa thế nào |
| :-- | :--- | :--- |
| 1 | **AI làm hộ luôn phần brainstorm.** Ngay từ đầu AI đã đưa ra trọn bộ ba ý tưởng prototype thay vì để nhóm tự nghĩ. Bài lab này có mục tiêu rèn khả năng brainstorm, nên phần đó lẽ ra phải là của người học. | Xem mục 4 — đây là nhận xét của chính người nộp, ghi lại đúng nguyên ý. |
| 2 | Mặc định bài lab chạy theo cấu trúc **3 người / 3 option / 3 tester**, trong khi nhóm chỉ có 2 người. | Chốt lại: giữ 3 options, mỗi người facilitate 1 phiên → **2 Feedback Notes**, và **ghi rõ đây là thiếu so với chuẩn** thay vì bịa phiên thứ ba. |
| 3 | Giả định repo Day 17 đã có sẵn **Solution Parking Lot**. Kiểm tra thì không có. | Dựng lại công khai từ hành vi trong hai practice note, ghi rõ trong Design Sheet rằng đây là bản **tái tạo**. |
| 4 | Bản nháp đầu của ba option nghiêng về mô tả **màn hình** — đúng anti-pattern *"3 options chỉ khác màu sắc, wording hoặc bố cục"*. | Ép lại theo trục agency: chốt **AI Act / Ask / Don't Act** trước, rồi mới thiết kế màn hình. Khoá 70% context, content và component cho cả ba. |
| 5 | Option C ban đầu chỉ có bản nháp "đúng và đẹp" — không có gì để tester phát hiện AI sai. | Cài một khối AI **suy diễn quá đà** (ngưỡng *10.000 tài liệu*) có nhãn vàng và dòng cơ sở nói rõ con số đó không có trong bài. |
| 6 | Code Option B để hiệu ứng xuất hiện chạy lại cho **mọi** thẻ ở mỗi lần re-render → cả rail nhấp nháy. | Phát hiện qua ảnh chụp Playwright. Bỏ animation, thay bằng nhãn tĩnh **MỚI**. |
| 7 | **Bug thật trong code AI viết:** biến trạng thái đặt tên `open` và `status` trùng với `document.open` / `window.status`, nên trong inline handler chúng trỏ nhầm đối tượng. Hậu quả: nút *Thu gọn* của Phương án D và nút *Xoá hết* của Option B **không hoạt động** — nhưng không báo lỗi gì. | Phát hiện khi test tự động thấy trạng thái không đổi sau khi bấm. Đổi tên biến và **định tuyến toàn bộ thao tác đổi state qua hàm có tên**, thay vì gán biến trực tiếp trong `onclick`. Chạy lại regression cho cả bốn prototype. |
| 8 | AI **không thể** và **không được** tạo Feedback Note. | Hai phiên test do người thật chạy. AI chỉ nhận field notes viết tay và biên tập lại; **mọi quote trong repo đều là lời tester thật**. Chỗ facilitator không quan sát được thì ghi là *không quan sát được*, không suy đoán ngược từ hành vi. |

---

## 3. Ranh giới evidence — khai báo rõ

| Loại nội dung | Nguồn |
| :--- | :--- |
| Quote của NV-01, NV-02 trong Evidence Snapshot | **Người thật**, từ 2 phỏng vấn ghi âm ngày 17/08/2026 của Day 17 |
| Quote của `T1`, `T2` trong hai Feedback Note | **Người thật**, từ 2 phiên test Day 18. Không ghi âm — facilitator ghi tay tại chỗ |
| Cột "Điều nhóm đang diễn giải" · khối `INTERPRETED` | **Diễn giải của nhóm**, tách riêng khỏi lời user |
| Bài học *Vector Database & RAG*, slide, lời giảng | **Nội dung dựng sẵn cho prototype** — không phải bài học có thật |
| Gợi ý của Option B, bản nháp của Option C, phần mở rộng của Phương án D | **Canned output**, viết tay sẵn — không gọi model |
| Ô "evidence được đọc hay bỏ qua" ở hai phiên | **Không đo được.** Ghi thẳng là không quan sát tách bạch được, không điền suy đoán |

---

## 4. Phần tự viết — Nguyễn Quang Vinh

**Chỗ AI hiểu sai bối cảnh nhóm mình nhất là gì?**

> Là về **mục đích**. Bài này nhằm rèn luyện khả năng brainstorm, mà bước đầu AI đã đi làm hết cho mình việc lên ý tưởng về prototype.

**Bạn tự quyết định khác với đề xuất của AI ở chỗ nào, và vì sao?**

> Mình có hỏi off-script trong lúc phỏng vấn, nhằm nắm được ý tưởng của người test — thay vì bám chặt bộ câu hỏi đã soạn sẵn. Chính từ đó mới ra được đề xuất ghép A và B.

**Sau khi test thật, điều gì trong thiết kế 3 option hoá ra là AI (và tôi) đoán sai?**

> Việc ghi chú **không nhằm tóm tắt đầy đủ nhất nội dung buổi học**. Ngược lại, với nhiều người, ghi chú là ghi lại những gì quan trọng / unconventional / đặc biệt / khó hiểu từ buổi học. Cả ba option đều được thiết kế trên giả định sai này, và Option C là chỗ giả định sai đó lộ rõ nhất.

**Về cách mình facilitate**

> Mình nhiều khi gợi ý lời nói cho người ta, làm người ta bị ngắt suy nghĩ — đúng vào những lúc họ đang im lặng suy nghĩ. Lần sau mình sẽ để họ tự tư duy, thay vì mớm lời.
