# AI Support Log — Day 18
## Trần Thị Vân Anh (MHV `2A202601411`) & Nguyễn Quang Vinh (MHV `2A202601049`) · Nhóm 2 · Case B — AI Notes

Lab cho phép dùng AI hỗ trợ sinh mã nguồn giao diện, tạo dữ liệu mẫu (*canned output*) và kiểm thử kỹ thuật; **không** dùng AI để thay thế con người trong việc phân tích bài toán, tư duy thiết kế, viết tài liệu (docs), tạo kịch bản test hay bịa đặt kết quả quan sát. Log này khai báo chính xác phạm vi hỗ trợ hạn chế của AI và khẳng định toàn bộ phần tài liệu (docs) & thiết kế là công việc do con người trực tiếp thực hiện.

---

## 1. Công việc của con người (Human Tasks — Con người tự thực hiện 100%)

**Nghiên cứu & Phân tích đầu vào**
* Đọc và phân tích tài liệu hướng dẫn Day 18, tổng hợp dữ liệu phỏng vấn NV-01 / NV-02 từ Day 17 để trích dẫn quote làm bằng chứng thực tế.
* Tự xây dựng bài toán **Hypothesis Problem** theo 5 thành phần (`situation / user / job / barrier / consequence`) và chỉ ra 4 điểm chưa được chứng minh.

**Viết tài liệu thiết kế & Đánh giá Human–AI**
* Tự lập **Solution Parking Lot** 6 hướng giải pháp dựa trên quan sát thực tế từ Day 17.
* Tự tư duy và xây dựng **Comparison Contract** (khóa 70% bối cảnh) cùng **Distance Check** để tạo 3 phương án A/B/C khác biệt về cơ chế thay vì giao diện.
* Tự phân tích và lập bảng **Human–AI Decision Table** (xác định mức độ agency `Don't Act → Ask → Act`, rủi ro khi AI sai và cơ chế phục hồi control).
* Trực tiếp viết toàn bộ nội dung văn bản trong các tài liệu thiết kế ([`README.md`](README.md), [`three-option-design-sheet.md`](three-option-design-sheet.md), [`prototype-link.md`](prototype-link.md)).

**Soạn kịch bản kiểm thử & Điều phối**
* Trực tiếp biên soạn **Test Prompt**, 5 điểm quan sát (**Observation Focus**), luật facilitation và bảng counterbalance cho các phiên test ([`test-script.md`](test-script.md)).
* Trực tiếp facilitate các phiên kiểm thử người dùng thật, tự tay ghi chép ghi chú kiểm thử ([`prototype-feedback-note.md`](prototype-feedback-note.md)) và tổng hợp bài học ([`group-feedback-synthesis.md`](group-feedback-synthesis.md)).

---

## 2. Phạm vi AI hỗ trợ (Hạn chế & Thuần kỹ thuật)

AI chỉ được sử dụng như một công cụ hỗ trợ kỹ thuật phụ trợ (*technical assistant*):

* **Sinh code boilerplate HTML/CSS/JS**: Hỗ trợ viết khung code HTML/CSS/JS thuần tự chứa cho 3 file prototype trong thư mục `prototype/` theo đúng thiết kế layout do nhóm đưa ra.
* **Tạo dữ liệu giả lập (Canned Output)**: Hỗ trợ sinh chuỗi văn bản mẫu cho 4 thẻ gợi ý (Option B) và 7 khối bản nháp (Option C) dựa trên kịch bản bài học mà nhóm đã biên soạn trước.
* **Rà soát & Test kỹ thuật**: Chạy thử luồng giao diện bằng Playwright để kiểm tra lỗi hiển thị/click trên giao diện trước khi mang đi test với người dùng.

---

## 3. Điểm sai / hạn chế của AI và cách nhóm tự xử lý

| # | Hạn chế / Đề xuất chưa phù hợp của AI | Con người đã tự xử lý / sửa đổi thế nào |
| :-- | :--- | :--- |
| 1 | AI gợi ý thiết kế 3 phương án chỉ khác biệt về giao diện/màu sắc (anti-pattern). | Nhóm bác bỏ hoàn toàn, tự định hình lại 3 phương án dựa trên trục **AI Agency** (`Don't Act / Ask / Act`) và phân quyền cho người dùng. |
| 2 | AI mặc định nhóm có 3 người theo tài liệu mẫu của bài lab. | Nhóm tự điều chỉnh phân công công việc (1 thành viên gánh 2 option & 2 phiên test) để đảm bảo chất lượng bài làm. |
| 3 | AI tạo bản nháp Option C "hoàn hảo", không có lỗi. | Nhóm chủ động yêu cầu cài 1 khối dữ liệu suy diễn quá đà (ngưỡng 10.000 tài liệu) để thử thách khả năng phát hiện lỗi của tester. |
| 4 | AI không thể thực hiện phỏng vấn hay viết phản hồi thật. | Toàn bộ tài liệu phỏng vấn và tổng hợp feedback được nhóm giữ trống hoàn toàn để điền từ phiên test thực tế với người dùng. |

---

## 4. Ranh giới bằng chứng (Evidence Boundaries)

* **Quote người dùng (NV-01, NV-02)**: 100% từ phỏng vấn người thật ở Day 17.
* **Tài liệu & Thiết kế**: 100% do con người trực tiếp suy nghĩ và biên soạn.
* **Code Prototype & Canned Data**: Có sự hỗ trợ sinh mã nguồn phụ trợ từ AI.
* **Ghi chép kiểm thử**: 100% người thật thực hiện và ghi nhận.

---

## 5. Phần tự viết — Thành viên nhóm

> Điền bằng lời của chính mình sau khi đã chạy phiên test. Đây là phần lab yêu cầu phải là phản ánh cá nhân, không được để AI viết hộ.

### Trần Thị Vân Anh — MHV `2A202601411`
* **Chỗ tôi thấy AI hiểu sai bối cảnh nhóm mình nhất:**
  > ……………………………………………………………………………………
* **Điều tôi tự quyết định khác với đề xuất của AI, và vì sao:**
  > ……………………………………………………………………………………
* **Sau khi test thật, điều gì trong thiết kế ba option hóa ra là AI đoán sai:**
  > ……………………………………………………………………………………

### Nguyễn Quang Vinh — MHV `2A202601049`
* **Chỗ tôi thấy AI hiểu sai bối cảnh nhóm mình nhất:**
  > ……………………………………………………………………………………
* **Điều tôi tự quyết định khác với đề xuất của AI, và vì sao:**
  > ……………………………………………………………………………………
* **Sau khi test thật, điều gì trong thiết kế ba option hóa ra là AI đoán sai:**
  > ……………………………………………………………………………………


