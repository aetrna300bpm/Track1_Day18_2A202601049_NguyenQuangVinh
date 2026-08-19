# Group Feedback Synthesis — Day 18
## Case B — AI Notes · Nhóm 2

---

## 0. Hai phiên đã chạy — và phiên thứ ba không có

| Phiên | Facilitator | Tester | Relevant context | Thứ tự chạy | Trạng thái |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **F1** | Nguyễn Quang Vinh | `T1` — ghi chú bằng Notepad | ✅ Có | A → B → C | ✅ Đã chạy · [note](prototype-feedback-note.md) |
| **F2** | Trần Thị Vân Anh | `T2` — ghi chú ra vở | ✅ Có | B → C → A | ✅ Đã chạy · [note](prototype-feedback-note-vananh.md) |
| ~~F3~~ | — | — | — | — | ❌ **Không có** |

> ⚠️ **Nhóm chỉ có 2 Feedback Notes, không phải 3.** Nhóm 2 người → 2 phiên, mỗi thành viên facilitate một phiên. Đây là **thiếu so với chuẩn của lab** (thiết kế cho nhóm 3 người). Ảnh hưởng cụ thể được nêu ở mục 4 chứ không giấu đi.

Hai tester được đảo thứ tự chạy để option cuối không được lợi thế vì tester đã quen giao diện. **Kết quả trùng nhau ở cả hai thứ tự** — đây là điểm làm nhóm tin hơn vào pattern bên dưới.

---

## 1. Bảng tổng hợp

| Nội dung | **Feedback 1** (`T1`, A→B→C) | **Feedback 2** (`T2`, B→C→A) | Pattern hoặc khác biệt |
| :--- | :--- | :--- | :--- |
| **First action** | **A:** gõ thẳng vào ô tự viết, không chạm slide · **B:** bấm *Thêm* trên thẻ · **C:** không làm gì | **B:** bấm *Thêm* trên thẻ · **C:** bấm qua tới hết · **A:** bấm sang slide tiếp, ghi rất ít | 🔴 **Pattern:** ở option nào cũng vậy, hành vi đầu tiên là **tự gõ hoặc bấm tiếp** — không ai bắt đầu bằng việc tương tác với nội dung slide |
| **Breakdown chính** | **A:** không biết bấm được vào chữ trong slide · **B:** tưởng thẻ đã tự nằm trong ghi chú, không biết phải bấm *Thêm* | **A:** khó hiểu tương tác đánh dấu · **B:** không biết phải bấm *Thêm* thì thẻ mới lưu | 🔴 **Pattern, hai lỗi độc lập:** (1) affordance đánh dấu của **A vô hình** với cả hai người; (2) cơ chế "phải duyệt thì mới lưu" của **B bị hiểu ngược** bởi cả hai người, ở cả hai thứ tự chạy |
| **Evidence đọc hay bỏ qua** | Không quan sát tách bạch được | Không đọc — *"đây là test UI, ai đọc slide làm gì"* | ⚠️ **Không kết luận được.** Cả hai phiên đều không đo được hành vi này — xem mục 4 |
| **Cách lấy lại control** | **B:** thấy nút *Sửa* nhưng lười, thà tự gõ · **C:** không sửa gì, và tới bước review vẫn không hiểu bản nháp | **B, C:** không sửa gì · **A:** không cần sửa, vì ghi chú là tự viết | 🔴 **Pattern:** khi phải sửa nội dung do AI đề xuất, **cả hai đều chọn tự gõ lại thay vì sửa**. Đường recovery mà nhóm thiết kế công phu ở B và C **không ai dùng** |
| **Option được chọn** | **A** | **A** | 🔴 **Pattern: cả hai chọn A** — ở hai thứ tự chạy khác nhau |
| **Trade-off** | Chấp nhận A dù **chính mình vừa vấp ở A**, vì cơ chế đúng; đề xuất đổi sang **bôi đen** và cho **AI mở rộng đoạn đã đánh dấu** | Chọn A vì *"ít tính năng, tự chủ cao"*; nhưng lo **ghi chú của mình khó hiểu khi đọc lại**, và đó là chỗ muốn AI elaborate | 🔴 **Pattern:** cả hai muốn AI ở vai trò **mở rộng cái mình đã chọn**, không phải **chọn giúp** |
| **Phản ứng với C** | *"chẳng liên quan gì đến ghi chú, out of scope… cũng chẳng cho ghi chú khi đang học thì dùng làm gì?"* | *"note cái gì vậy, cho vào AI tóm tắt cho nhanh"* | 🔴 **Pattern mạnh nhất:** cả hai **bác C ở mức khái niệm, không phải mức giao diện**. Không ai chê nút, chê màu hay chê bố cục — họ nói **đây không phải ghi chú** |

### Khác biệt rõ nhất giữa hai người

Hai tester **hành xử giống nhau nhưng đánh giá bằng hai thước đo khác nhau**:

* `T1` đánh giá theo **"cái này cho tôi cái gì"** — nói về scope, về personalize, về việc option nào đáng tồn tại.
* `T2` đánh giá theo **"cái này có dễ dùng không"** — nói về nhanh, tiện, ít tính năng.

Nhóm cho rằng khác biệt đến từ nền tảng: một người có kinh nghiệm làm sản phẩm hơn, một người thuần end user. **Điều đáng chú ý là hai thước đo khác nhau vẫn dẫn tới cùng một lựa chọn.**

---

## 2. Ba câu chốt

### Một Next Change nhóm chốt

> **Ghép Option A và Option B thành một cơ chế duy nhất:** giữ *người dùng tự đánh dấu* làm cơ chế chính, **đổi thao tác đánh dấu từ bấm-vào-dòng sang bôi đen**, và để **AI mở rộng đúng những đoạn đã được đánh dấu — chỉ khi người dùng bấm yêu cầu, ở cuối bài**. Bỏ hoàn toàn cơ chế AI tự chọn nội dung của Option C.

*(Thuộc dạng hợp lệ: "kết hợp hai options nhưng giữ một cơ chế chính rõ ràng".)*
Đã dựng thành **Phương án D** trong [`prototype-v2/`](prototype-v2/index.html) — chi tiết ở [`three-option-design-sheet.md`](three-option-design-sheet.md#chặng-6--sau-khi-test--phương-án-d).

### Evidence nào dẫn tới quyết định này

1. **Cả hai tester đều chọn A**, ở hai thứ tự chạy ngược nhau — nên không phải hiệu ứng thứ tự.
2. **`T1` tự đề xuất chính giải pháp này**, không bị gợi ý: đánh dấu bằng bôi đen, rồi *"khi người dùng đánh dấu nội dung slide (nội dung slide thường rất vắn tắt) thì AI có thể hỗ trợ elaborate nội dung cho idea/keyword đó"*.
3. **`T2` mô tả cùng một mong muốn bằng lời khác**: *"tự ghi lại các điểm chưa rõ vào note, giao AI làm rõ các note"* — và nêu đúng lý do cần AI: *"các ghi chú có thể khó hiểu khi đọc lại"*.
4. **Cơ chế confirm-từng-thẻ của B bị bác bằng chi phí cụ thể**, không phải cảm tính: *"cúi xuống đọc cái ngẩng lên là không hiểu gì rồi"* — chi phí thật là **mất mạch nghe giảng**, không phải vài giây thao tác. Vì vậy bản gộp **không** đặt bước duyệt nào trong lúc học.
5. **Affordance của A hỏng ở cả hai người** (`T1` không biết bấm được; `T2` thấy khó hiểu) → giữ cơ chế nhưng **phải đổi thao tác**, không phải giữ nguyên rồi thêm hướng dẫn.

### Still Unproven sau hai feedback

* **Điều gì làm việc ghi chú trở nên hữu ích với số đông vẫn chưa biết.** Hai tester có hai phong cách ghi chú khác nhau (Notepad vs viết tay), và hai thước đo đánh giá khác nhau. Hai người không nói được gì về số đông.
* **Bôi đen có dễ khám phá hơn bấm-vào-dòng hay không — chưa test.** Đó mới là giả thuyết rút ra từ lời tester, chưa phải kết quả.
* **Toàn bộ phần thiết kế evidence & uncertainty chưa được kiểm chứng.** Không phiên nào đo được tester có đọc chip nguồn hay badge *"AI suy ra"* không (mục 4).
* **Chưa ai từng gặp AI mở rộng SAI.** Bản gộp có nhãn *"AI thêm — không có trong bài"* nhưng chưa người nào chạm vào tình huống đó.
* **Thiếu phiên thứ ba**, nên mọi "pattern" ở trên thực chất là "hai trên hai" — đủ để định hướng iteration, không đủ để loại trừ trùng hợp.

### Đối chiếu với 4 điều "chưa chứng minh" từ Chặng 1

| # | Điều chưa chứng minh (Chặng 1) | Sau 2 phiên |
| :-- | :--- | :--- |
| 1 | Học viên chịu bỏ bao nhiêu thao tác trong lúc nghe giảng | 🔽 **Lung lay theo hướng rõ:** họ muốn thao tác ít nhất có thể, chỉ giữ cái thật cần, để tập trung vào lời giảng |
| 2 | Có tin & dùng lại ghi chú AI tự viết mà mình không đánh dấu | 🔽 **Lung lay mạnh:** cả hai đều không tin và không thấy hữu ích, đặc biệt ở khoản *AI chọn hộ chỗ nào quan trọng* |
| 3 | "Đủ" của một bản ghi chú là keyword hay tóm tắt đầy đủ | 🔽 **Đảo hướng giả định của nhóm:** với cả hai người, ghi chú **không phải bản tóm tắt** mà là *ghi lại những gì cần chú ý để review sau* |
| 4 | 2 practice interview chưa phải validation | ⏸️ **Vẫn nguyên.** Thêm 2 phiên prototype test không biến practice interview thành validation |

---

## 3. Câu nhóm được phép kết luận

> *"Với Hypothesis Problem này, chúng tôi đã thử ba cách giải. Hai tester ngoài nhóm, chạy ở hai thứ tự khác nhau, đều chọn cách giải do người dùng tự đánh dấu (A) và đều bác cách giải AI tự viết bản nháp (C) ở mức khái niệm — họ nói đó không phải ghi chú. Vì vậy iteration tiếp theo chúng tôi giữ cơ chế đánh dấu của A, đổi thao tác sang bôi đen, và chuyển AI từ vai trò chọn-nội-dung sang vai trò mở-rộng-theo-yêu-cầu."*

Câu nhóm **không** kết luận:

> ~~"User đã xác nhận solution này đúng."~~
> ~~"Option A là phương án thắng."~~
> ~~"Bôi đen dễ dùng hơn bấm-vào-dòng."~~ *(chưa test)*

---

## 4. Hạn chế của chính đợt test này

1. **Hai Feedback Notes, không phải ba.** Nhóm 2 người. Mọi pattern ở trên là "hai trên hai".
2. **Không đo được hành vi đọc evidence.** Cả hai facilitator đều không thiết lập cách quan sát riêng cho việc tester có đọc chip nguồn / badge uncertainty hay không. Đây là lỗi thiết kế phương pháp của nhóm, không phải kết quả về sản phẩm — và nó làm **Gate 3 (Human control) chưa được kiểm chứng bằng hành vi**, dù đã được thiết kế đầy đủ.
3. **Bối cảnh test làm giảm động lực đọc nội dung.** `T2` nói thẳng: *"đây là test UI tính năng, ai đọc slide làm gì"*. Nội dung bài học trong prototype vì vậy được đối xử như chữ trang trí, khác với tình huống học thật.
4. **Facilitator phiên 1 tự nhận có mớm lời** cho tester vào lúc họ đang im lặng suy nghĩ. Một số câu trả lời ở phiên 1 có thể đã bị định hướng.
5. **Canned output.** Không phiên nào nói được gì về chất lượng nội dung mà AI thật sẽ sinh ra.

---

## 5. Sau Next Change — cần test gì tiếp

| Câu hỏi | Cách kiểm ở vòng sau |
| :--- | :--- |
| Bôi đen có tự hiện ra không? | Đưa Phương án D cho một tester **chưa từng thấy A/B/C**, đo xem họ có đánh dấu được mà không cần nhắc không |
| Người dùng có thật sự bấm *"Làm rõ giúp tôi"* không? | Đếm số mục được yêu cầu mở rộng trên tổng số mục đã đánh dấu |
| Có ai đọc phần AI mở rộng không, hay chỉ bật lên rồi bỏ đó? | Hỏi sau: *"chỗ này nó lấy từ đâu ra?"* thay vì cố quan sát bằng mắt |
| Người dùng có bắt được khi AI thêm thứ không có trong bài không? | Quan sát phản ứng với nhãn *"AI thêm — không có trong bài"* ở mục *cosine similarity* |
