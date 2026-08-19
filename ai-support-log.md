# AI Support Log — Day 18
## Trần Thị Vân Anh (Case Lead · MHV `2A202601411`) & Nguyễn Quang Vinh (MHV `2A202601049`) · Nhóm 2 · Case B — AI Notes

Lab cho phép dùng AI làm công cụ hỗ trợ phụ trợ (dọn dẹp định dạng Markdown, dựng khung code HTML/CSS từ specification chi tiết của con người, kiểm thử giao diện tự động, rà soát chính tả); **không** cho phép dùng AI để tạo quote/observation/feedback giả mạo, sáng tạo thay cho người học phần ý tưởng giải pháp (idea), hay viết hộ phần đóng góp và reflection cá nhân. 

Log này khai báo đúng nguyên tắc cốt lõi của nhóm: **Con người (Vân Anh & Vinh) nắm giữ 100% ý tưởng (idea), định hướng và biên soạn toàn bộ tài liệu chính (doc chính); AI chỉ đóng vai trò trợ lý kỹ thuật / định dạng tối thiểu.**

---

## 1. Phân định vai trò: Con người (Idea & Doc chính) vs. AI (Hỗ trợ tối thiểu)

### 🧑‍💻 Con người tự thực hiện 100% (Idea, Thiết kế & Documentation chính)
* **Ý tưởng & Định hình bài toán (Idea & Problem Statement):** Phân tích dữ liệu phỏng vấn Day 17 (NV-01 & NV-02), trực tiếp cô đọng thành Hypothesis Problem chuẩn 5 thành phần và xác định 4 điều chưa được chứng minh.
* **Sáng tạo 3 Solution Options & Trục Agency:** Tự tư duy và đề xuất 3 hướng giải pháp khác biệt về cơ chế dựa trên phân cấp quyền hạn Human–AI:
  * **Option A (Marker-first):** AI ở chế độ `Don't Act` (chỉ gom đúng vết user tự đánh dấu).
  * **Option B (Live suggestion rail):** AI ở chế độ `Ask` (gợi ý thời gian thực để user duyệt).
  * **Option C (Auto recap):** AI ở chế độ `Act` (tự viết nháp, user review sau).
* **Xây dựng khung so sánh & Ma trận phân quyền:** Tự lập Comparison Contract, Distance Check và Human–AI Decision Table (đủ 5 hàng cho A/B/C/D).
* **Biên soạn toàn bộ tài liệu chính (Doc chính):** Tự tay nghiên cứu và viết 100% nội dung các tài liệu:
  * [`three-option-design-sheet.md`](three-option-design-sheet.md) (Chặng 1–4 & thiết kế Phương án D)
  * [`README.md`](README.md) (Tổng quan dự án, phân công nhóm, Gate đối chiếu)
  * [`test-script.md`](test-script.md) (Kịch bản test, 5 điểm Observation Focus, counterbalance)
  * [`group-feedback-synthesis.md`](group-feedback-synthesis.md) (Tổng hợp 2 phiên test, Next Change & Still Unproven)
* **Thực thi phỏng vấn & Thu thập evidence thật:** Trực tiếp facilitate 2 phiên test thực tế với tester ngoài nhóm (`T1`, `T2`), tự tay ghi chép field notes tại chỗ ([`prototype-feedback-note.md`](prototype-feedback-note.md) & [`prototype-feedback-note-vananh.md`](prototype-feedback-note-vananh.md)).
* **Tổng hợp bài học & Đề xuất Phương án D:** Từ 4 pattern trùng khớp thu được sau 2 phiên test, nhóm tự rút ra bài học cốt lõi và tự thiết kế **Phương án D (Next Change)** gộp ưu điểm của A và B.

### 🤖 AI hỗ trợ những gì (Tối thiểu & Phụ trợ)
* **Định dạng & Trình bày (Formatting):** Rà soát lỗi chính tả, căn chỉnh bảng biểu Markdown cho đẹp mắt và chuẩn hóa tiêu đề trong các file doc do nhóm tự viết.
* **Khung Code HTML/CSS tĩnh (Boilerplate Code):** Sinh khung code HTML/CSS/JS tĩnh cho 4 prototype (`prototype/index.html`, `option-a/b/c.html`, `prototype-v2/index.html`) **dựa trên đúng specification, wireframe và bố cục chi tiết do nhóm con người quy định**.
* **Dữ liệu giả lập (Content Fixture):** Đưa nội dung bài học giả lập (*Vector Database & RAG cơ bản*, 3 slide, 3 câu lời giảng) và các canned output vào code prototype theo đúng kịch bản thiết kế của nhóm.
* **Kiểm thử tự động (Technical Verification):** Hỗ trợ viết script Playwright chạy kiểm tra hiển thị giao diện prototype trên trình duyệt.

---

## 2. Điểm sai / hời hợt của AI và cách con người đã xử lý

| # | AI làm sai / hời hợt | Con người đã phát hiện và xử lý thế nào |
| :-- | :--- | :--- |
| 1 | **AI có xu hướng đề xuất các giải pháp tự động hóa ôm đồm**, tự đưa ra ý tưởng làm thay người dùng. | **Bác bỏ hoàn toàn.** Nhóm ép thiết kế về đúng 3 mức Agency (`Don't Act`, `Ask`, `Act`) dựa trên quan sát thực tế từ Day 17 để giữ quyền chủ động cho người học. |
| 2 | AI mặc định cấu trúc bài lab cho nhóm **3 người / 3 tester / 3 feedback notes**. | **Tự điều chỉnh.** Nhóm giữ nguyên thực tế nhóm có 2 người, chia nhau facilitate 2 phiên test (`T1`, `T2`) -> lập **2 Feedback Notes** và ghi rõ đây là điểm chưa đạt chuẩn lab thay vì dùng AI bịa phiên thứ ba. |
| 3 | AI giả định repo Day 17 đã có sẵn Solution Parking Lot. | **Kiểm tra và tái lập.** Nhóm kiểm tra repo cũ thấy không có file này, nên tự dựng lại Parking Lot 6 hướng từ đúng hành vi quan sát ở Day 17 và ghi rõ trong Design Sheet. |
| 4 | Bản nháp code giao diện đầu tiên do AI sinh ra nghiêng về khác **mô tả màn hình** thay vì khác **cơ chế**. | **Tự tái cấu trúc.** Nhóm khóa 70% context, content fixture và component dùng chung, chỉ cho phép khác biệt ở vị trí ra quyết định và cơ chế AI tương tác. |
| 5 | **Bug thật trong code AI sinh ra:** Biến trạng thái đặt tên `open` và `status` trùng với thuộc tính toàn cục (`document.open` / `window.status`) khiến các nút tương tác bị đơ. | **Phát hiện & Refactor:** Trong quá trình test, nhóm phát hiện nút *Thu gọn* (Phương án D) và nút *Xoá hết* (Option B) không phản hồi. Nhóm đã tự debug, đổi tên biến và định tuyến toàn bộ thao tác đổi state qua hàm xử lý có tên. |
| 6 | AI không thể tự nhận biết được tâm lý / rào cản nhận thức của tester trong phiên phỏng vấn. | **Con người trực tiếp quan sát:** Nhóm tự nhận ra tester bị mất mạch nghe giảng ở B và bị quá tải ở C, từ đó đưa ra kết luận bác bỏ Option C ở mức khái niệm. |

---

## 3. Ranh giới Evidence — Khai báo minh bạch

| Loại nội dung | Nguồn gốc & Độ xác thực |
| :--- | :--- |
| Quote của NV-01, NV-02 trong Evidence Snapshot | **100% Người thật**, từ 2 phỏng vấn ghi âm ngày 17/08/2026 (Day 17). |
| Quote của `T1`, `T2` trong 2 Feedback Note | **100% Người thật**, từ 2 phiên test thực tế Day 18 do Vinh và Vân Anh trực tiếp ghi chép tại chỗ. |
| Cột "Điều nhóm đang diễn giải" / khối `INTERPRETED` | **Tư duy của nhóm con người**, được phân tách rõ ràng với phát ngôn gốc của user. |
| Bài học *Vector Database & RAG*, slide, lời giảng | **Dữ liệu giả lập (Content fixture)** dựng cho prototype — không phải dữ liệu thu từ người dùng. |
| Gợi ý của Option B, bản nháp Option C, phần mở rộng Phương án D | **Canned output** do nhóm thiết kế sẵn để đưa vào prototype. |
| Quan sát về việc đọc chip nguồn / badge AI | **Không đo được.** Nhóm ghi thẳng là không quan sát được, tuyệt đối không dùng AI suy đoán điền bừa. |

---

## 4. Phần tự phản ánh (Reflection) — Trần Thị Vân Anh & Nguyễn Quang Vinh

**Chỗ AI hiểu sai bối cảnh và vai trò nhất là gì?**
> AI thường coi mình là trung tâm giải pháp và cố gắng tự động hóa toàn bộ trải nghiệm. Tuy nhiên, bài lab này nhằm rèn luyện tư duy thiết kế Human–AI và khả năng làm chủ sản phẩm của con người. Nhóm đã chủ động giới hạn AI chỉ làm các tác vụ định dạng/code phụ trợ, còn bản thân nhóm tự đưa ra ý tưởng và tự viết toàn bộ tài liệu chính.

**Con người tự quyết định khác với đề xuất ban đầu của AI ở điểm nào, và vì sao?**
> Trong lúc phỏng vấn, facilitator (Vinh & Vân Anh) đã chủ động hỏi off-script khi thấy tester lúng túng, thay vì bám cứng kịch bản AI hỗ trợ soạn. Chính nhờ những câu hỏi đào sâu thực tế đó mà nhóm thu được insight quan trọng: *"Ghi chú là để personalize và lưu lại điều chưa hiểu/quan trọng"*, từ đó tự nghĩ ra Phương án D (kết hợp A và B).

**Sau khi test thật, điều gì trong thiết kế mà cả nhóm và AI từng đoán sai?**
> Nhóm và AI từng giả định rằng *ghi chú = bản tóm tắt đầy đủ bài học*. Sau 2 phiên test thực tế với `T1` và `T2`, cả hai tester đều bác bỏ giả định này. Họ khẳng định ghi chú phải do họ tự chọn lọc (personalize), AI tự viết trọn gói (Option C) làm mất đi ý nghĩa của việc ghi chú.

**Bài học về facilitation của con người:**
> Người facilitate (đặc biệt ở phiên 1) nhận thấy mình đôi lúc có xu hướng mớm lời cho tester khi họ im lặng suy nghĩ. Bài học rút ra là cần giữ khoảng lặng để quan sát đúng phản ứng tự nhiên của người dùng.
