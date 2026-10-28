# BÀI LÀM – HACKATHON 01

- **Mã đề:** 15
- **Họ tên:Nguyễn Đức Hiếu** 
- **Lớp:HN-KS26-CNTT2** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):WINDOWS** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# Hiển thị đường dẫn tuyệt đối của thư mục hiện tại:
 C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website>
# Liệt kê toàn bộ nội dung:
 Get-ChildItem -Recurse -Force
# Di chuyển các file:
mv bang_gia_goi.txt docs/
mv logo_studio_anh.PNG media/
# Sao chép logo từ media vào backup:
cp media/logo_studio_anh.PNG
mv logo_studio_anh.PNG backup/
# Xóa file .tmp:
rm temp_238.tmp
# Dùng đường dẫn tương đối vào logs,liệt kê nội dung rồi quay lại đường dẫn:
C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website> cd logs
C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website\logs> Get-ChildItem -Recurse -Force
C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website\logs> cd..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
    Directory: C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:42 PM                backup
d-----        10/28/2026   1:45 PM                data
d-----        10/28/2026   1:41 PM                docs
d-----        10/28/2026   1:45 PM                logs
d-----        10/28/2026   1:41 PM                media
-a----        10/27/2026   1:32 AM             71 .env
-a----        10/27/2026   1:32 AM           2225 bai_lam.md
-a----        10/27/2026   1:32 AM             59 bang_gia_goi.txt
-a----        10/27/2026   1:32 AM           7231 logo_studio_anh.PNG
-a----        10/27/2026   1:32 AM             22 temp_238.tmp


    Directory: C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6099 lich_chup_thang_5.xlsx


    Directory: C:\Users\Vivobook\Downloads\starter-kit (1)\starter-kit\studio_anh_website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           1088 studio.log

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
 Get-Content logs/studio.log | Select-String "ERROR" | Measure-Object

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-05-28 07:29:30 [ERROR] Tai anh len may chu that bai
2026-05-28 07:44:30 [ERROR] Tai anh len may chu that bai

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Script:auto_report.ps1
# Tac gia:Nguyen Duc Hieu
# Ngay tao:28/10/2026

Write-Host "Dang loc log..."
"===BAO CAO LOI==="> logs/auto_report.txt
Get-Content logs/studio.log | Select-String "ERROR">> logs/auto_report.txt

Write-Host "Hoan thanh!"
```

### Kết quả hiển thị

```text
2026-05-28 07:29:30 [ERROR] Tai anh len may chu that bai
2026-05-28 07:44:30 [ERROR] Tai anh len may chu that bai
2026-05-28 07:47:30 [ERROR] Het thoi gian cho (timeout)
2026-05-28 07:50:30 [ERROR] Khong tim thay trang /album-moi (404)
2026-05-28 08:11:30 [ERROR] Khong tim thay trang /album-moi (404)
2026-05-28 08:14:30 [ERROR] Het thoi gian cho (timeout)
2026-05-28 08:17:30 [ERROR] Tai anh len may chu that bai
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
Get-Content logs/studio.log | Select-String "ERROR" | Measure-Object

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
7

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell


```

### Nội dung file logs/tong_hop.txt

```text


```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/lich_chup_thang_5.xlsx`, không cần ghi vào đây.
