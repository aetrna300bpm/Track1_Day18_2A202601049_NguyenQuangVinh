# Prototype Feedback Note — Phiên 1
## Facilitator: **Nguyễn Quang Vinh** (MHV `2A202601049`) · Tester `T1`
### Case B — AI Notes · Day 18 · Nhóm 2

---

## 0. Thông tin phiên

| Mục | Nội dung |
| :--- | :--- |
| **Facilitator** | Nguyễn Quang Vinh — MHV `2A202601049` |
| **Tester** | `T1` — người ngoài nhóm ✅ |
| **Relevant context** | ✅ **Có.** Trả lời câu hỏi tuyển: *"Có, ghi bằng Notepad"* |
| **Thứ tự chạy** | **A → B → C** |
| **Ghi âm** | Không — ghi tay trong lúc quan sát |

> Tester có đúng hành vi nền mà nhóm giả định từ Day 17: **ghi chú bằng Notepad**, trùng với `NV-02` ở practice interview.

---

## 1. Bảng quan sát

| Observation | Option A — Marker-first | Option B — Live rail | Option C — Auto recap |
| :--- | :--- | :--- | :--- |
| **First action** | Gõ thẳng vào ô ghi chú tự viết rồi bấm *Thêm*. **Không chạm vào nội dung slide.** | Bấm nút *Thêm* trên thẻ gợi ý | Không làm gì. Chỉ bấm qua slide cho tới hết |
| **Chỗ dừng, do dự hoặc hiểu sai** | Không nhận ra là **bấm được vào các dòng nội dung slide** để đánh dấu. Giao diện không hướng dẫn gì | Không hiểu là **phải bấm *Thêm* thì thẻ mới vào ghi chú** — tưởng các thẻ đã tự nằm sẵn trong ghi chú và chỉ mất đi nếu bị xoá | Không có chỗ dừng nào, vì luồng này tự động hoàn toàn — tester không phải quyết định gì |
| **Evidence được đọc hay bỏ qua** | ⚠️ Facilitator **không quan sát tách bạch được** hành vi đọc chip nguồn ở phiên này — xem mục 4 | ⚠️ Không quan sát tách bạch được | Không để ý gì mấy tới nội dung bản nháp |
| **Cách tester sửa hoặc lấy lại control** | Tự viết ghi chú của mình. **Không có nội dung sai để sửa** — ghi chú ở A hoàn toàn dựa vào người dùng | Có nhìn thấy nút *Sửa* nhưng **lười dùng — thà tự gõ lại còn hơn** | Không sửa gì. Đọc tới phần review cuối bài thì **vẫn không hiểu bản nháp nói gì** |
| **Option được chọn** | ✅ **A** | | |
| **Lý do và trade-off** | Chọn A vì **tính cá nhân hoá cao nhất**. Tester cho rằng vấn đề của A **chỉ nằm ở chỗ hướng dẫn chưa rõ và chưa intuitive**, chứ không nằm ở cơ chế. Đề xuất: cho đánh dấu bằng **bôi đen** thay vì bấm-vào-dòng, vì như vậy đánh dấu nhanh được chỗ mình không hiểu. Đồng thời thấy **giá trị của B có thể ghép vào A**: khi user đánh dấu một đoạn slide (vốn rất vắn tắt) thì **AI mở rộng nội dung cho ý/keyword đó**. | | |
| **Muốn tự làm phần nào** | Phần **ghi note** — *"đây là phần cá nhân hóa"* | | |
| **Evidence chống lại kỳ vọng của nhóm** | Nhóm dự đoán tester sẽ đánh dấu ≥2 chỗ rồi mới bấm tạo. Thực tế **tester không hề biết là bấm được vào chữ trong slide**; hành vi đầu tiên là gõ note tay ở chỗ cần dựa vào slide | Nhóm dự đoán tester sẽ *bấm Thêm mà không đọc lý do*. Thực tế nặng hơn: **tester thấy chính việc phải bấm nút là phiền** | Nhóm dự đoán tester sẽ *bấm Lưu thẳng* — tức là vẫn coi bản nháp là thứ đáng lưu. Thực tế tester **bác bỏ ý tưởng ở mức khái niệm**, thấy tính năng hoàn toàn không hữu ích |

### Quote nguyên văn

> **[Option A]** *"Em không biết là bấm được vào chữ trong slide để ghi note đấy."*

> **[Option B]** *"Cái này hơi ngố, người dùng phải confirm nội dung và bấm lưu thì tốn thời gian, đặc biệt là khi phải confirm nội dung, cúi xuống đọc cái ngẩng lên là không hiểu gì rồi."*

> **[Option C]** *"Mình thấy cái này chẳng liên quan gì đến ghi chú, out of scope. Ghi chú nhằm personalize còn cái này thì viết hết hộ, cũng chẳng cho ghi chú khi đang học thì dùng làm gì?"*

**Facilitator có phải giải thích hộ tester không?** Không có chỗ nào ngoài ba câu cứu hộ đã quy định.

---

## 2. Tách bốn lớp

```
OBSERVED
- Ở A, hành vi đầu tiên là gõ vào ô tự viết. Tester không chạm vào slide, và
  nói thẳng là không biết chữ trong slide bấm được.
- Ở B, tester bấm Thêm nhưng hiểu sai cơ chế: tưởng thẻ đã nằm sẵn trong ghi
  chú và chỉ mất đi nếu bị xoá. Thấy nút Sửa nhưng không dùng, chọn tự gõ.
- Ở B, tester mô tả chi phí của việc confirm bằng chính trải nghiệm nghe giảng:
  "cúi xuống đọc cái ngẩng lên là không hiểu gì rồi".
- Ở C, tester không thao tác gì trong suốt bài, và tới bước review thì nói vẫn
  không hiểu bản nháp nói gì.
- Tester chọn A, và chủ động đề xuất hai thay đổi cụ thể: đánh dấu bằng bôi đen,
  và cho AI mở rộng đúng đoạn đã đánh dấu.

INTERPRETED  (diễn giải của nhóm — có thể sai)
- Cơ chế của A không sai, nhưng affordance của nó vô hình. Một hành vi
  "bấm vào dòng chữ" không phải thứ người học tự nghĩ ra khi đang xem bài giảng.
- Ở B, chi phí thật không phải là số lần bấm mà là chi phí CHUYỂN SỰ CHÚ Ý.
  Mỗi lần confirm buộc tester rời khỏi mạch nghe giảng, và cái mất là mạch hiểu
  bài chứ không phải vài giây thao tác.
- Ở C, thứ bị bác không phải giao diện mà là ĐỊNH NGHĨA. Với tester này, ghi chú
  là hành vi cá nhân hoá; một bản tóm tắt do máy viết hộ không phải là ghi chú,
  dù nó đúng và đầy đủ.

DECIDED — NEXT CHANGE
Ghép A và B: giữ cơ chế người dùng tự đánh dấu làm cơ chế chính, đổi thao tác
đánh dấu từ bấm-vào-dòng sang BÔI ĐEN, và để AI mở rộng đúng những đoạn đã được
đánh dấu — chỉ khi người dùng bấm yêu cầu, ở cuối bài.
Đã dựng thành `prototype-v2/` (Phương án D).

STILL UNPROVEN
- Một người không đủ để nói bôi đen thì dễ khám phá hơn bấm-vào-dòng. Đó vẫn
  là giả thuyết, chưa test.
- Không biết tester có đọc chip nguồn hay không — facilitator không tách bạch
  được hành vi này (xem mục 4).
- Không biết tester sẽ phản ứng thế nào nếu AI mở rộng SAI, vì ở phiên này
  chưa có cơ chế nào để tester bắt gặp AI sai.
```

---

## 3. Điều phiên này KHÔNG chứng minh được

* Tester chọn A **sau khi đã vấp ở chính A**. Việc chọn A vì thấy cơ chế đúng, không có nghĩa bản A hiện tại dùng được.
* Cả ba option đều dùng **canned output**, nên phiên này **không** nói gì về chất lượng nội dung AI thật sẽ sinh ra.
* Đây là một người. Không đủ để kết luận gì về value, chỉ đủ để chỉ ra chỗ vỡ.

---

## 4. Ghi chú về phương pháp — hạn chế của chính phiên này

Ô **"evidence được đọc hay bỏ qua"** trong sheet ghi chép **không dùng được ở phiên này**. Facilitator không thiết lập cách quan sát riêng cho hành vi đọc chip nguồn (`Slide 6`, `Lời giảng 18:05`, badge `AI suy ra`), nên không phân biệt được *tester đọc rồi bỏ qua* với *tester không nhìn thấy*.

Hệ quả: **toàn bộ phần thiết kế evidence & uncertainty của Chặng 3 chưa được kiểm chứng** ở phiên này. Ghi lại đây thay vì suy đoán ngược từ hành vi.

Lần sau: hoặc quay màn hình có con trỏ, hoặc hỏi một câu duy nhất sau khi tester xong option — *"chỗ này nó lấy từ đâu ra?"* — thay vì cố quan sát bằng mắt trong lúc facilitate.

---

## 5. Tự đánh giá cách facilitate

Facilitator **có vi phạm luật facilitation**: nhiều lần gợi ý lời cho tester đúng vào lúc tester đang im lặng suy nghĩ, làm ngắt mạch tư duy của họ.

Lần sau: để im lặng chạy hết, đếm thầm tới 5, không mớm lời.
