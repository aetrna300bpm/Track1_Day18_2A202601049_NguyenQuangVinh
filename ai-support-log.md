# AI Support Log — Day 18
## Trần Thị Vân Anh (`2A202601411`) & Nguyễn Quang Vinh (`2A202601049`) · Nhóm 2 · Case B

Tài liệu này ghi nhận chi tiết và minh bạch toàn bộ các tác vụ hỗ trợ kỹ thuật, xử lý định dạng, khởi tạo dữ liệu mẫu và kiểm thử tự động do AI thực hiện trong quá trình triển khai dự án Day 18.

---

## 1. Chi tiết các công việc AI đã hỗ trợ

### 📄 Đọc và xử lý tài liệu đầu vào (Input Processing)
* **Phân tích yêu cầu bài lab:** Đọc và tổng hợp 10 file PDF hướng dẫn cùng slide guide Day 18 để trích xuất 6 chặng thực hiện, 5 Gate kiểm định chất lượng và danh sách các anti-pattern cần tránh.
* **Ánh xạ dữ liệu phỏng vấn:** Đọc repository Day 17 của nhóm để trích xuất và ánh xạ các câu quote cùng observation từ 2 bài phỏng vấn thô (NV-01 và NV-02) vào bảng cấu trúc Evidence Snapshot.

### 📝 Định dạng & Biên tập Markdown (Markdown Formatting)
* **Rà soát & Chuẩn hóa:** Rà soát lỗi chính tả, căn chỉnh khoảng cách, chuẩn hóa tiêu đề và định dạng bảng biểu Markdown trong các tài liệu thiết kế.
* **Đồng bộ hiển thị:** Đảm bảo toàn bộ file Markdown tuân thủ chuẩn CommonMark/GFM để hiển thị đồng nhất và sạch đẹp trên GitHub Markdown renderer.

### 💻 Sinh khung Code Prototype HTML/CSS/JS (Code Generation)
* **Dựng khung giao diện tĩnh:** Sinh code HTML/CSS/JS thuần cho 4 prototype: `prototype/index.html` (Trang Hub), `option-a.html` (Marker-first), `option-b.html` (Live suggestion rail), `option-c.html` (Auto recap) và `prototype-v2/index.html` (Phương án D).
* **Cam kết kỹ thuật:** Đảm bảo code tự chứa (self-contained), không gọi thư viện CDN bên ngoài, không lưu trữ dữ liệu local storage để đảm bảo tính độc lập khi test.
* **Tái sử dụng component visual:** Xây dựng giao diện visual dùng chung gồm Header, Player mock, Panel bên phải, Bảng màu và các nút điều hướng (`Bắt đầu lại` / `Tất cả phương án`).

### 📊 Tạo dữ liệu mẫu & Canned Output (Mock Data & Fixtures)
* **Nội dung bài học giả lập:** Dựng nội dung bài học mẫu *Vector Database & RAG cơ bản* gồm 3 slide chính và 3 câu lời giảng chi tiết ngoài slide tại các mốc thời gian `12:40`, `18:05`, `24:30`.
* **Canned AI Output:** Tạo sẵn các đầu ra mẫu cho AI:
  * 4 thẻ gợi ý ghi chú theo thời gian thực cho Option B.
  * Bản nháp 7 khối ghi chú tự động cho Option C.
  * 12 đoạn giải thích mở rộng cho Phương án D.

### 🧪 Hỗ trợ Kiểm thử Giao diện Tự động (Automated UI Testing)
* **Script Playwright:** Viết script kiểm thử tự động với Playwright để giả lập thao tác bấm nút, chuyển trang và re-render giao diện trên trình duyệt Chromium.
* **Chụp ảnh kiểm thử:** Tự động chụp ảnh màn hình các trạng thái tương tác để phát hiện nhanh các lỗi vỡ layout hoặc lỗi hiển thị giao diện.

---

## 2. Điểm sai, giới hạn & Lỗi kỹ thuật của AI

* **Lỗi xung đột tên biến JS (Bug trùng tên thuộc tính trình duyệt):** Trong code khởi tạo ban đầu cho Option B và Phương án D, AI đặt tên biến trạng thái là `open` và `status`. Các tên biến này trùng với thuộc tính toàn cục của trình duyệt (`document.open` / `window.status`), khiến cho các hàm sự kiện inline (`onclick`) trỏ sai đối tượng. Hậu quả là nút *Thu gọn* ở Phương án D và nút *Xoá hết* ở Option B bị liệt hoàn toàn.
* **Lỗi nhấp nháy giao diện (Re-render Animation Bug):** Ở Option B, AI viết logic re-render chạy lại toàn bộ hiệu ứng xuất hiện cho tất cả các thẻ ở mỗi lần thêm/sửa, khiến toàn bộ thanh gợi ý bị nhấp nháy liên tục khi người dùng thao tác.
* **Lỗi thiếu điểm test AI sai (Flawless Output Bug):** Trong Option C ban đầu, AI tạo ra một bản recap hoàn hảo không có lỗi sai nào, khiến cho tester không có cơ hội kiểm tra xem người dùng có thực sự phát hiện ra khi AI suy diễn sai hay không.
* **Thiếu khả năng nhận biết trải nghiệm người dùng:** AI không thể tự đo lường được cảm xúc, sự phân tâm hay mức độ bị ngắt mạch nghe giảng của tester trong quá trình tương tác.

---

## 3. Ranh giới dữ liệu tuyệt đối của AI

* **Không giả mạo Quote & Observation:** 100% các câu trích dẫn, nhận xét và phản hồi trong mọi tài liệu đều xuất phát từ phỏng vấn thực tế với người thật (NV-01, NV-02 ở Day 17 và T1, T2 ở Day 18). AI tuyệt đối không tự sinh ra bất kỳ câu quote giả mạo nào.
* **Tách biệt rõ ràng dữ liệu:** AI tuân thủ việc phân định rõ đâu là phát ngôn trực tiếp của user, đâu là phần diễn giải của người học và đâu là dữ liệu mẫu dựng sẵn cho prototype.
* **Không suy đoán khi thiếu bằng chứng:** Với các hành vi không quan sát được trong phiên test (như việc tester có đọc chip nguồn hay badge nhãn hay không), AI ghi nhận *không quan sát được* chứ không tự tiện suy đoán điền bừa.
