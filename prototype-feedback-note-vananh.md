# Prototype Feedback Note — Phiên 2
## Facilitator: **Trần Thị Vân Anh** (MHV `2A202601411`) · Tester `T2`
### Case B — AI Notes · Day 18 · Nhóm 2

> Bản này thuộc phiên do Vân Anh facilitate. Đưa vào repo cá nhân của Vinh để nhóm có đủ bộ dữ liệu tổng hợp; note thuộc phiên Vinh facilitate nằm ở [`prototype-feedback-note.md`](prototype-feedback-note.md).

---

## 0. Thông tin phiên

| Mục | Nội dung |
| :--- | :--- |
| **Facilitator** | Trần Thị Vân Anh — MHV `2A202601411` |
| **Tester** | `T2` — người ngoài nhóm ✅ |
| **Relevant context** | ✅ **Có.** Trả lời câu hỏi tuyển: *"Có, ghi ra vở"* |
| **Thứ tự chạy** | **B → C → A** *(đảo so với phiên 1 để option cuối không được lợi vì tester đã quen giao diện)* |
| **Ghi âm** | Không — ghi tay trong lúc quan sát |

---

## 1. Bảng quan sát

| Observation | Option B — Live rail *(chạy đầu)* | Option C — Auto recap | Option A — Marker-first *(chạy cuối)* |
| :--- | :--- | :--- | :--- |
| **First action** | Bấm *Thêm* trên các thẻ gợi ý | Bấm qua liên tục cho tới hết bài | Bấm sang slide tiếp theo. **Tester này ghi rất ít** |
| **Chỗ dừng, do dự hoặc hiểu sai** | Không biết **phải bấm *Thêm* thì thẻ mới được lưu lại** | Không có — luồng không yêu cầu thao tác nào | **Khó hiểu tương tác đánh dấu nội dung slide** |
| **Evidence được đọc hay bỏ qua** | **Không đọc.** Facilitator ghi nhận thêm bối cảnh: đây là phiên test giao diện nên tester không có động lực đọc nội dung slide | Không để ý — vì không có tương tác nào buộc phải nhìn | Có bấm vào các dòng chữ trong slide |
| **Cách tester sửa hoặc lấy lại control** | Không sửa gì | Không sửa gì | Không cần sửa — ghi chú là do tự viết |
| **Option được chọn** | | | ✅ **A** |
| **Lý do và trade-off** | Chọn **A** vì *"cảm giác ít tính năng, tự chủ cao"*. Muốn **tự ghi các điểm chưa rõ vào note, rồi giao AI làm rõ các note đó**. Điều chưa thoải mái: **ghi chú của chính mình có thể khó hiểu khi đọc lại** — và đó là chỗ AI nên hỗ trợ elaborate. | | |
| **Evidence chống lại kỳ vọng của nhóm** | Nhóm dự đoán tester sẽ duyệt thẻ mà không đọc lý do. Thực tế: **tester không quan tâm tới việc AI sinh ghi chú**, vẫn chỉ tự ghi lại chỗ nào cần note hoặc chưa rõ | Nhóm dự đoán tester sẽ *bấm Lưu thẳng*. Thực tế: **tester không quan tâm bản ghi chú do AI viết**, và tự đề xuất phương án thay thế là dán vào AI ngoài | Nhóm dự đoán tester sẽ *giật mình vì ghi chú thiếu*. Thực tế: **tester đánh dấu rất ít**, nên không đủ nội dung để đến được khoảnh khắc đó |

### Quote nguyên văn

> **[Option B]** *"Thế này thì ghi chú chẳng bằng quick note, review lại hết hơi."*

> **[Option C]** *"Thế này thì note cái gì vậy, cho vào AI tóm tắt cho nhanh."*

> **[Option A]** *"Cái này tiện phết, được cái nhanh."*

**Facilitator có phải giải thích hộ tester không?** Không.

---

## 2. Tách bốn lớp

```
OBSERVED
- Ở B, tester bấm Thêm nhưng không biết rằng nếu không bấm thì thẻ không được lưu
  — cùng một hiểu sai với tester T1 ở phiên 1, dù thứ tự chạy khác nhau.
- Ở B và C, tester không đọc nội dung nguồn.
- Ở C, tester không thao tác gì và nói thẳng là sẽ mang sang AI ngoài cho nhanh.
- Ở A, tester nói tương tác đánh dấu khó hiểu, nhưng vẫn bấm được vào chữ trong
  slide, và vẫn đánh dấu rất ít.
- Tester chọn A và mô tả mong muốn: tự ghi điểm chưa rõ, giao AI làm rõ lại.

INTERPRETED  (diễn giải của nhóm — có thể sai)
- Việc T2 vẫn "khó hiểu" nhưng vẫn bấm được, còn T1 thì hoàn toàn không phát hiện
  ra, cho thấy affordance của A nằm ở vùng nửa vời: đủ để mò ra nếu chịu thử,
  không đủ để tự hiện ra.
- Câu "ghi chú chẳng bằng quick note" và "cho vào AI tóm tắt cho nhanh" nói cùng
  một điều: nếu sản phẩm bắt trả thêm chi phí thao tác mà không đổi lại thứ gì
  workaround hiện tại chưa có, người dùng sẽ quay về workaround.
- Mong muốn "tự ghi, giao AI làm rõ" đặt AI ở vai trò MỞ RỘNG cái người dùng đã
  chọn, không phải vai trò CHỌN GIÚP. Đây là điểm trùng với đề xuất của T1.

DECIDED — NEXT CHANGE
Cùng kết luận với phiên 1: ghép A và B, giữ cơ chế người dùng tự đánh dấu, và
để AI mở rộng đúng phần đã đánh dấu khi được yêu cầu. Đã dựng thành
`prototype-v2/` (Phương án D).

STILL UNPROVEN
- Không biết tester sẽ đánh dấu nhiều hơn không nếu thao tác đánh dấu dễ hơn —
  T2 đánh dấu ít, nhưng không rõ vì thao tác khó hay vì phong cách ghi chú của
  họ vốn đã ít.
- Bối cảnh "đang test UI" làm tester không đọc nội dung bài học. Không biết
  trong tình huống học thật họ có đọc không.
```

---

## 3. Ghi chú về phương pháp

Facilitator nêu rõ một hạn chế của chính bối cảnh test: **tester biết mình đang test giao diện**, nên không có động lực đọc nội dung bài học như khi học thật. Điều này ảnh hưởng trực tiếp tới mọi quan sát về *evidence được đọc hay bỏ qua* ở phiên này — và nhóm không dùng phiên này để kết luận gì về phần thiết kế evidence & uncertainty.
