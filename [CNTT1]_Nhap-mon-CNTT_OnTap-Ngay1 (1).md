# BÀI LÀM NGÀY 1 — NHẬP MÔN CNTT

- Họ và tên: Nguyễn Bùi Gia Bảo
- Lớp: CNTT1

## PHẦN A — TỔ CHỨC THƯ MỤC BẰNG GUI

### A1. Hiển thị đuôi file và file ẩn
- Thực hiện trên File Explorer/Finder.

### A2. Đổi tên thư mục gốc
- Tên mới: `trung-tam-tieng-anh`

### A3. Tạo thư mục
- `docs`
- `media`
- `data`
- `logs`
- `archive`

### A4. Đổi tên file theo snake_case
| Tên ban đầu | Tên mới |
|---|---|
| `Logo Trung Tam.PNG` | `logo_trung_tam.png` |
| `Anh Lop Hoc.JPG` | `anh_lop_hoc.jpg` |
| `Lich Hoc.txt` | `lich_hoc.txt` |
| `Hoc Vien Khoa 3.xlsx` | `hoc_vien_khoa_3.xlsx` |
| `Access.log` | `access.log` |

### A5. Di chuyển file bằng GUI
- `hoc_vien_khoa_3.xlsx` → `data`
- `access.log` → `logs`
- Giữ logo, ảnh lớp học, lịch học và hai file `.tmp` tại thư mục gốc.

### A6. Sao chép file mẫu
- Sao chép `bai_lam_ngay1.md` vào thư mục gốc.
- Giữ `.env` tại thư mục gốc; không upload lên GitHub.
## PHẦN B — THAO TÁC BẰNG CLI

### B1. Hiển thị đường dẫn tuyệt đối
```powershell
pwd
```
**Kết quả:** Dán đường dẫn thực tế hiển thị trên máy.

### B2. Liệt kê nội dung, gồm file ẩn
```powershell
Get-ChildItem -Force
```

### B3. Di chuyển file
```powershell
Move-Item .\lich_hoc.txt .\docs\
Move-Item .\logo_trung_tam.png .\media\
Move-Item .\anh_lop_hoc.jpg .\media\
```

### B4. Sao chép logo vào archive
```powershell
Copy-Item .\media\logo_trung_tam.png .\archive\
```

### B5. Xóa hai file tạm
```powershell
Remove-Item .\temp_201.tmp
Remove-Item .\temp_202.tmp
```

### B6. Truy cập logs bằng đường dẫn tương đối
```powershell
cd .\logs
Get-ChildItem
cd ..
```

### B7. Sao chép ảnh bằng đường dẫn tương đối
```powershell
cd .\docs
Copy-Item ..\media\anh_lop_hoc.jpg ..\archive\
cd ..
```

### B8. Liệt kê toàn bộ dự án, gồm file ẩn
```powershell
Get-ChildItem -Force -Recurse
```
**Kết quả:** Thnhaf công
