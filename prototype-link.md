# Prototype Links
## Case B — AI Notes · Day 18 · Nhóm 2

---

## 1. Bộ A / B / C — bản đã mang đi test

Tester **luôn bắt đầu từ hub**, không mở thẳng vào một option.

| | Link |
| :--- | :--- |
| 🔷 **Hub — bắt đầu ở đây** | https://aetrna300bpm.github.io/Track1_Day18_2A202601049_NguyenQuangVinh/prototype/ |
| Phương án A — Marker-first | …/prototype/option-a.html |
| Phương án B — Live suggestion rail | …/prototype/option-b.html |
| Phương án C — Auto recap | …/prototype/option-c.html |

> **Bản deploy dùng trong hai phiên test** *(Trần Thị Vân Anh deploy để tester truy cập)*: `<<https://chipper-basbousa-bccf28.netlify.app>>`

Ba prototype này **giữ nguyên trạng thái lúc test**, không sửa sau khi có feedback — chúng là bằng chứng đi kèm hai Feedback Notes.

## 2. Phương án D — bản gộp A+B sau khi test

| | Link |
| :--- | :--- |
| ✨ **Phương án D** | https://aetrna300bpm.github.io/Track1_Day18_2A202601049_NguyenQuangVinh/prototype-v2/ |

Đây là **Next Change đã dựng thành prototype**, chưa được test với ai. Không dùng để so sánh với A/B/C, vì nó ra đời **sau** và **nhờ** hai phiên test đó. Thiết kế: [`three-option-design-sheet.md` §6](three-option-design-sheet.md#chặng-6--sau-khi-test--phương-án-d).

> Truy cập link online : https://leafy-frangipane-a83e8b.netlify.app

> Nếu chưa bật GitHub Pages, tất cả các file chạy được **offline**: tải repo về và mở `prototype/index.html` hoặc `prototype-v2/index.html` bằng trình duyệt. Không cần server, không cần cài gì.
>
> **Bật GitHub Pages:** repo → *Settings* → *Pages* → *Source: Deploy from a branch* → `main` / `/ (root)` → *Save*.

---

## 3. Trong repo

```
prototype/                 # bản đã test — KHÔNG sửa sau feedback
├── index.html             # Hub: bối cảnh + task chung + 3 nút A/B/C (không mô tả cơ chế)
├── option-a.html          # Marker-first  — AI Don't Act cho tới khi user bấm
├── option-b.html          # Live rail     — AI Ask ở từng mốc trong bài
└── option-c.html          # Auto recap    — AI Act (sinh nháp), user gate ở bước Lưu

prototype-v2/              # Next Change — chưa test
└── index.html             # Phương án D  — bôi đen → AI im lặng → user gọi → AI mở rộng
```

Mỗi file là **một file HTML tự chứa**: CSS và JS inline, không CDN, không network, không lưu trữ trình duyệt. Mở bằng `file://` cũng chạy đủ.

---

## 4. Điểm chung — khoảng 70% (Comparison Contract)

Áp dụng cho **cả bốn** file, kể cả Phương án D:

* **Bài học:** *Bài 4 — Vector Database & RAG cơ bản*, 32 phút.
* **Content fixture:** cùng 3 slide (Slide 5 / 6 / 7) và cùng 3 câu giảng viên nói thêm ngoài slide tại `12:40`, `18:05`, `24:30`.
* **Task:** rời bài học với một bản ghi chú đủ tin để ôn, có cả phần ngoài slide.
* **Component & style:** cùng header, cùng player mock, cùng panel phải, cùng bảng màu, cùng chip nguồn.
* **Reset path:** mọi option có **Bắt đầu lại** (về đầu bài học, xoá sạch state) và một nút quay về hub / về bộ A/B/C.

## 5. Điểm khác — critical interaction

| | Trong lúc học | Cuối bài | AI agency |
| :--- | :--- | :--- | :--- |
| **A** | User bấm vào dòng để highlight / bấm "Chưa hiểu" / gõ note. AI **không làm gì**. | User bấm *Tạo ghi chú từ N dấu* → AI gom đúng N dấu đó | **Don't Act** → Act hẹp khi được gọi |
| **B** | AI đẩy 4 thẻ gợi ý kèm nguồn + lý do; user Thêm / Sửa / Bỏ qua từng thẻ | Ghi chú = các thẻ user đã duyệt + phần user tự viết | **Ask** ở từng mốc |
| **C** | User **không phải làm gì** | AI tự viết bản nháp 7 khối có 3 mức độ chắc chắn; user Giữ / Sửa / Bỏ rồi mới Lưu | **Act** nhưng không commit |
| **D** *(chưa test)* | User **bôi đen** đoạn bất kỳ → *Đánh dấu* / *Chưa hiểu*; hoặc tự gõ. AI **im lặng hoàn toàn** | Mỗi mục có nút *✨ Làm rõ giúp tôi*; AI mở rộng **đúng đoạn đã đánh dấu**, hiện thu gọn bên dưới chữ của user | **Don't Act** → **Act khi được gọi**, từng mục một |

---

## 6. Lưu ý khi test

* Prototype dùng **canned output** — không gọi model thật, không API. Đúng phạm vi "vừa đủ để test" của lab.
* Nút `▶ Tiếp tục bài giảng` tua bài học qua **3 khoảnh khắc giảng dạy** thay vì phát đủ 32 phút.
* Trước mỗi tester, bấm **Bắt đầu lại**.
* Không có onboarding, không responsive hoàn chỉnh, không catalog lỗi — cố ý, theo scope của Chặng 4.
* Ở **Phương án D**, thao tác chính là **bôi đen chữ bằng chuột** (hoặc chạm-giữ trên di động), không phải bấm.
