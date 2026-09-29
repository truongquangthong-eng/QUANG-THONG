# CLAUDE.md — Quy tắc làm việc chung

Repo này là "trí nhớ" của công ty cho Claude: hồ sơ tóm tắt từng dự án, nhật ký quyết định, mẫu biểu và công cụ.
File gốc (bản vẽ, Revit, BOQ, hợp đồng, ảnh) **không** lưu ở đây mà nằm trên **OneDrive**.

## Ngôn ngữ và phong cách
- Luôn trả lời bằng **tiếng Việt**, văn phong chuyên nghiệp, có cấu trúc, đi thẳng vào vấn đề.
- Đơn vị: mm cho kích thước cấu kiện, m cho cao độ và chiều dài tuyến, m³ / m² / tấn cho khối lượng.
- Tiêu chuẩn tham chiếu: TCVN hiện hành; định mức theo Thông tư của Bộ Xây dựng còn hiệu lực.

## Làm việc với một dự án
Trước khi làm bất kỳ việc gì liên quan tới một dự án:
1. Đọc `du-an/DANH-SACH-DU-AN.md` để xác định mã dự án.
2. Đọc `du-an/<ma-du-an>/HO-SO-DU-AN.md` để nắm bối cảnh (chủ đầu tư, quy mô, lưới trục, cao độ, tiết diện, đường dẫn OneDrive).
3. Đọc `du-an/<ma-du-an>/NHAT-KY.md` để biết các quyết định đã chốt và lỗi đã gặp. **Không làm trái quyết định đã chốt** nếu chủ dự án chưa đồng ý.
4. Tìm file gốc theo đường dẫn OneDrive ghi trong hồ sơ dự án.

Sau khi làm xong:
- Quyết định kỹ thuật mới, số liệu đã chốt, lỗi đã gặp → ghi thêm vào `NHAT-KY.md` của dự án (mới nhất ở trên cùng).
- Số liệu trích xuất (tọa độ trục, cọc, móng, bảng khối lượng) → lưu CSV/JSON trong `du-an/<ma-du-an>/du-lieu/`.
- Không tự bịa thông tin dự án. Thông tin chưa có ghi `_(chưa có)_` và hỏi lại chủ dự án.

## Cloud hay máy?
| Cần gì | Làm ở đâu |
|---|---|
| AutoCAD / Revit đang mở (dựng model, dim, tag, join) | **Máy** — Claude Code cài trên máy, đọc thẳng thư mục OneDrive đã đồng bộ |
| Chỉ cần file, dữ liệu, Internet (báo cáo, tiến độ, hồ sơ thầu, code) | **Cloud** — qua connector Microsoft 365 hoặc file đưa lên repo |

## Quy ước đặt tên
- Mã dự án: chữ thường, không dấu, nối bằng gạch ngang (`nakano`, `kamiichino`, `tan-hy`).
- File báo cáo: `YYYY-MM-DD_<ma-du-an>_<loai>.<ext>`, ví dụ `2026-09-29_nakano_bao-cao-tuan.docx`.
- Ngày tháng: định dạng `YYYY-MM-DD`.

## Thêm dự án mới
1. Sao chép thư mục `du-an/_mau/` thành `du-an/<ma-du-an>/`.
2. Điền `HO-SO-DU-AN.md`.
3. Thêm một dòng vào `du-an/DANH-SACH-DU-AN.md`.

## Không đưa lên repo
File CAD/Revit/PDF/ảnh gốc, hợp đồng, thông tin tài chính mật của chủ đầu tư, mật khẩu, khóa API. Xem `.gitignore`.
