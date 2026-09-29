# QUANG-THONG — Hệ thống quản lý dự án xây dựng

Kho tri thức và công cụ dùng chung giữa chủ dự án và Claude (cloud và máy).

## Mô hình 3 lớp
| Lớp | Công cụ | Chứa gì |
|---|---|---|
| ① Điều hành | Notion / Excel | Tiến độ, đầu việc, vướng mắc, thanh toán |
| ② Hồ sơ | **OneDrive** | Bản vẽ CAD/DXF, Revit, BOQ, hợp đồng, biên bản, ảnh hiện trường |
| ③ Trí nhớ & tự động hóa | **Repo này** | Hồ sơ tóm tắt dự án, nhật ký quyết định, số liệu trích xuất, mẫu, công cụ |

## Cấu trúc
```
QUANG-THONG/
├─ CLAUDE.md                 Quy tắc chung — Claude đọc đầu tiên
├─ du-an/
│   ├─ DANH-SACH-DU-AN.md    Bảng tổng hợp các dự án
│   ├─ _mau/                 Khung mẫu cho dự án mới
│   ├─ nakano/
│   ├─ kamiichino/
│   └─ tan-hy/
│       ├─ HO-SO-DU-AN.md    Thông tin cốt lõi + đường dẫn OneDrive
│       ├─ NHAT-KY.md        Quyết định đã chốt, lỗi đã gặp
│       └─ du-lieu/          Số liệu trích xuất (CSV/JSON)
├─ mau/                      Mẫu báo cáo, biên bản, thư chào giá
└─ cong-cu/                  Script, add-in Revit
```

## Cách giao việc cho Claude
- "Làm báo cáo tuần dự án Nakano"
- "Cập nhật hồ sơ dự án Tân Hỷ: chủ đầu tư là …, khởi công …"
- "Ghi vào nhật ký Kamiichino: chốt cao độ ±0.000 = +3.250 so với cốt tự nhiên"
- "Tổng hợp tình hình cả 3 dự án"
