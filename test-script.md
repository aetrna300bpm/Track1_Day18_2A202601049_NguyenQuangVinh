# Test Prompt & Observation Focus — Chặng 5
## Kịch bản chạy phiên test A/B/C · Case B — AI Notes

> In ra hoặc mở song song khi facilitate. **Một phiên = 20 phút = một tester = cả A/B/C.**
>
> ✅ **Đã dùng thật cho 2 phiên Day 18.** Kết quả ở [`prototype-feedback-note.md`](prototype-feedback-note.md) và [`prototype-feedback-note-vananh.md`](prototype-feedback-note-vananh.md). Phần "cần sửa cho lần sau" ở mục 7.

---

## 1. Chuẩn bị trước khi tester tới

* [ ] Mở sẵn `prototype/index.html` (hoặc link GitHub Pages) trong một tab.
* [ ] Kiểm tra cả ba option đã bấm **Bắt đầu lại** để về trạng thái sạch.
* [ ] Chuẩn bị chỗ ghi: bản `prototype-feedback-note.md` trống.
* [ ] Xin phép ghi âm/ghi hình nếu muốn. Không bắt buộc — có thể chỉ ghi tay.
* [ ] **Thứ tự A/B/C cho tester này** (xem bảng counterbalance ở mục 5): ⟶ `____________`

---

## 2. Chốt context và task

### 2.1. Relevant context — một câu hỏi, tối đa 2 phút

> *"Gần đây bạn có từng học một bài học hoặc video trực tuyến mà bạn phải tự ghi chú lại để sau này xem lại không?"*

Nếu **có** → hỏi thêm đúng một câu: *"Lần đó bạn ghi bằng gì?"* rồi dừng, vào task.

Nếu **chưa từng** → vẫn chạy được phiên test. Ghi rõ vào Feedback Note là tester **không có relevant context**, và **không** dùng phiên này để đưa ra value claim mạnh — chỉ dùng để tìm interaction breakdown.

### 2.2. Outcome task — nói kết quả cần đạt, không nói nút cần bấm

> *"Trong tình huống này, hãy dùng từng phương án để **đi hết bài học và kết thúc với một bản ghi chú mà bạn tin là đủ để ôn lại trước kỳ kiểm tra** — trong đó có cả phần giảng viên nói thêm ngoài slide."*

Nói đúng một lần, ở đầu mỗi option. Không thêm gì.

### 2.3. Observation focus — năm thứ cần quan sát

| # | Quan sát | Cụ thể là gì ở bài này |
| :-- | :--- | :--- |
| 1 | **First action** | Mở ra thì tester chạm/bấm gì đầu tiên? Có bấm ▶ ngay, hay đọc panel phải trước? |
| 2 | **Hesitation** | Dừng ở đâu, bao lâu, trước nút nào? (A: trước nút "Chưa hiểu"; B: trước thẻ bị khóa; C: trước nút Lưu) |
| 3 | **Evidence đọc hay bỏ qua** | Có bấm/đọc chip nguồn `Từ Slide 6` / `Lời giảng 18:05` và chip vàng `AI suy ra — hãy kiểm tra` không? |
| 4 | **Correction / recovery** | Khi thấy nội dung sai hoặc thiếu thì làm gì: sửa, bỏ, hoàn tác, quay lại bài học — hay kệ? |
| 5 | **Option được chọn + trade-off** | Chọn A/B/C nào cho tình huống này, vì sao, và **chấp nhận đánh đổi gì**? |

---

## 3. Luật facilitation

1. **Tester tự điều khiển prototype.** Không cầm chuột hộ.
2. **Dùng cùng một task** cho cả A, B và C.
3. **Không narrate, không giải thích icon** hay ý nghĩa màu.
4. **Không lấp im lặng.** Đếm thầm tới 5 trước khi mở miệng.
5. **Không hỏi "Bạn có thích không?"**
6. Khi tester hỏi cách nó hoạt động → hỏi ngược: **"Theo bạn, nó nên hoạt động như thế nào?"**

**Ba câu cứu hộ — chỉ dùng ba câu này**

* *"Bạn cứ nói to suy nghĩ của mình nhé."*
* *"Bạn sẽ làm gì tiếp theo?"*
* *"Theo bạn, nó nên hoạt động như thế nào?"*

---

## 4. Timeline 20 phút

| Thời gian | Hoạt động | Ghi chú cho facilitator |
| :--- | :--- | :--- |
| **0–2** | Make comfortable + hỏi relevant context | Đọc opening ở mục 4.1 |
| **2–14** | Tester dùng A/B/C — **~4 phút mỗi option** | Sau mỗi option: bấm **Tất cả phương án** rồi mở option kế. Không bình luận giữa các option |
| **14–18** | So sánh, lý do và trade-off | Ba câu ở mục 4.2 |
| **18–20** | Hoàn thành Feedback Note cá nhân | Ghi ngay, đừng để tới sau |

### 4.1. Opening — đọc nguyên văn

> *"Chúng mình đang thử ba cách thiết kế, không kiểm tra bạn. Không có câu trả lời đúng hoặc sai. Bạn hãy tự thao tác và nói to điều mình đang nghĩ; mình sẽ cố gắng không hướng dẫn."*

### 4.2. Compare — sau khi đã chạy cả ba

* *"Trong tình huống này, bạn chọn A, B hay C? Vì sao?"*
* *"Bạn muốn tự làm phần nào và giao cho AI phần nào?"*
* *"Điều gì ở phương án đã chọn khiến bạn chưa thoải mái?"*

---

## 5. Ba tester và thứ tự A/B/C

Ba phiên độc lập, mỗi phiên một facilitator, tester phải là **người ngoài nhóm**. Ưu tiên người có relevant context (đang học online).

Đảo thứ tự giữa ba phiên để giảm order effect — nếu ai cũng chạy A→B→C thì option cuối luôn được lợi vì tester đã quen giao diện.

| Phiên | Facilitator | Tester | Thứ tự chạy | Trạng thái |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Nguyễn Quang Vinh | `T1` — ghi chú bằng Notepad | **A → B → C** | ✅ đã chạy |
| 2 | Trần Thị Vân Anh | `T2` — ghi chú ra vở | **B → C → A** | ✅ đã chạy |
| ~~3~~ | — | — | ~~C → A → B~~ | ❌ không có — nhóm chỉ 2 người |

> Người phụ trách thiết kế một option **vẫn phải cho tester chạy cả ba**, không chỉ mang option của mình đi test.

---

## 6. Ba lỗi dễ mắc nhất trong phiên này

* **Giải thích hộ.** Nếu tester bí ở B vì không hiểu vì sao nút Thêm bị khóa — **đó chính là kết quả cần ghi**, không phải sự cố cần cứu.
* **Ghi "tester thích B".** Vô nghĩa nếu không kèm tester *đã làm gì* và *đánh đổi gì*.
* **Kết luận sau ba người.** Ba feedback là input cho iteration tiếp theo, không phải bằng chứng solution đã validated.

---

## 7. Sau khi chạy thật — kịch bản này hỏng ở đâu

Ghi lại để lần sau không lặp:

1. **Ô "evidence được đọc hay bỏ qua" không đo được bằng mắt.** Cả hai facilitator đều không tách bạch được *tester đọc rồi bỏ qua* với *tester không nhìn thấy*. Hậu quả: toàn bộ phần thiết kế evidence & uncertainty của Chặng 3 chưa được kiểm chứng.
   → **Lần sau:** quay màn hình có con trỏ, **hoặc** hỏi đúng một câu sau khi tester xong mỗi option: *"chỗ này nó lấy từ đâu ra?"*
2. **Bối cảnh "đang test UI" làm tester không đọc nội dung bài học.** `T2` nói thẳng: *"đây là test UI tính năng, ai đọc slide làm gì."*
   → **Lần sau:** mở đầu bằng một câu neo vào việc học thật, không nói "test giao diện".
3. **Facilitator phiên 1 mớm lời** cho tester đúng vào lúc họ im lặng suy nghĩ.
   → **Lần sau:** đếm thầm tới 5 trước khi mở miệng, chỉ dùng đúng ba câu cứu hộ.
4. **Ô "Ngày & thời lượng" không ai điền** — không mang lại thông tin gì cho phân tích.
   → **Lần sau:** bỏ khỏi sheet.
