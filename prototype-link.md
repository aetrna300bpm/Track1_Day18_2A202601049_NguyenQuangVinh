# Prototype Links — A / B / C
## Case B — AI Notes · Day 18 · Nhóm 2

Ba micro-prototype dùng chung một bài học, một content fixture và một bộ visual component. Chỉ **critical interaction** khác nhau.

---

## 1. Link chung của nhóm

Tester **luôn bắt đầu từ hub**, không mở thẳng vào một option:

| | Link Deploy Netlify (Live) | Link GitHub Pages |
| :--- | :--- | :--- |
| 🔷 **Hub — bắt đầu ở đây** | **https://chipper-basbousa-bccf28.netlify.app/prototype/** | https://aetrna300bpm.github.io/Track1_Day18_2A202601049_NguyenQuangVinh/prototype/ |
| Phương án A (Marker-first) | https://chipper-basbousa-bccf28.netlify.app/prototype/option-a.html | …/prototype/option-a.html |
| Phương án B (Live Rail) | https://chipper-basbousa-bccf28.netlify.app/prototype/option-b.html | …/prototype/option-b.html |
| Phương án C (Auto Recap) | https://chipper-basbousa-bccf28.netlify.app/prototype/option-c.html | …/prototype/option-c.html |

> 🌐 **Link Deploy chính thức**: [https://chipper-basbousa-bccf28.netlify.app](https://chipper-basbousa-bccf28.netlify.app) (hoặc trực tiếp Hub [https://chipper-basbousa-bccf28.netlify.app/prototype/](https://chipper-basbousa-bccf28.netlify.app/prototype/)).
>
> 📁 **Offline**: Ba file cũng chạy được trực tiếp bằng cách tải repo về và mở `prototype/index.html` trên trình duyệt mà không cần server hay kết nối mạng.

---

## 2. Trong repo

```
prototype/
├── index.html      # Hub: bối cảnh chung + task chung + 3 nút A/B/C (không mô tả cơ chế)
├── option-a.html   # Marker-first  — AI Don't Act cho tới khi user bấm
├── option-b.html   # Live rail     — AI Ask ở từng mốc trong bài
└── option-c.html   # Auto recap    — AI Act (sinh nháp), user gate ở bước Lưu
```

Mỗi file là **một file HTML tự chứa**: CSS và JS inline, không CDN, không network, không lưu trữ trình duyệt. Mở bằng `file://` cũng chạy đủ.

---

## 3. Điểm chung — khoảng 70% (Comparison Contract)

* **Bài học:** *Bài 4 — Vector Database & RAG cơ bản*, 32 phút.
* **Content fixture:** cùng 3 slide (Slide 5 / 6 / 7) và cùng 3 câu giảng viên nói thêm ngoài slide tại `12:40`, `18:05`, `24:30`.
* **Task:** rời bài học với một bản ghi chú đủ tin để ôn, có cả phần ngoài slide.
* **Component & style:** cùng header, cùng player mock, cùng panel phải, cùng bảng màu, cùng chip nguồn.
* **Reset path:** mọi option có **Bắt đầu lại** (về đầu bài học, xóa sạch state) và **Tất cả phương án** (về hub).

## 4. Điểm khác — critical interaction

| | Trong lúc học | Cuối bài | AI agency |
| :--- | :--- | :--- | :--- |
| **A** | User highlight / bấm "Chưa hiểu" / gõ note. AI **không làm gì**. | User bấm *Tạo ghi chú từ N dấu* → AI gom đúng N dấu đó | **Don't Act** → Act hẹp khi được gọi |
| **B** | AI đẩy 4 thẻ gợi ý kèm nguồn + lý do; user Thêm / Sửa / Bỏ qua từng thẻ | Ghi chú = các thẻ user đã duyệt + phần user tự viết | **Ask** ở từng mốc |
| **C** | User **không phải làm gì** | AI tự viết bản nháp 7 khối có 3 mức độ chắc chắn; user Giữ / Sửa / Bỏ rồi mới Lưu | **Act** nhưng không commit |

---

## 5. Lưu ý khi test

* Prototype dùng **canned output** — không gọi model thật, không API. Đúng phạm vi "vừa đủ để test" của lab.
* Nút `▶ Tiếp tục bài giảng` tua bài học qua **3 khoảnh khắc giảng dạy** thay vì phát đủ 32 phút.
* Trước mỗi tester, bấm **Bắt đầu lại** ở cả ba option.
* Không có onboarding, không responsive hoàn chỉnh, không catalog lỗi — cố ý, theo scope của Chặng 4.
