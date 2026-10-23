# ÔN TẬP HACKATHON 01 – NHẬP MÔN CNTT

**Chủ đề:** Đánh giá chất lượng kỹ năng Nhập môn Công nghệ thông tin
**Ngày thi thử:** Thứ Sáu, 23/10/2026
**Thời gian:** 90 phút

## 1. Phần 4.1 – Tổ chức thư mục bằng GUI

### 1.1. Cấu trúc thư mục

```text
van-phong-pham-website/
├── .env
├── bai_lam.md
├── logo_van_phong_pham.png
├── nhap_hang.txt
├── temp_131.tmp
├── README.md
├── docs/
├── media/
│   └── logo_van_phong_pham.png
├── data/
│   └── don_ban_thang_10.xlsx
├── logs/
│   └── shop.log
└── backup/
    └── logo_van_phong_pham.png
```

### 1.2. Các bước thực hiện

1. Bật hiển thị phần mở rộng tên file và file ẩn trong File Explorer hoặc Finder.
2. Đổi tên thư mục gốc thành `van-phong-pham-website`.
3. Tạo 5 thư mục: `docs`, `media`, `data`, `logs`, `backup`.
4. Đổi tên các file theo chuẩn `snake_case`:

   * `Logo Van Phong Pham.PNG` → `logo_van_phong_pham.png`
   * `Nhap Hang.txt` → `nhap_hang.txt`
   * `Don Ban Thang 10.xlsx` → `don_ban_thang_10.xlsx`
   * `Shop.log` → `shop.log`
5. Chuyển `don_ban_thang_10.xlsx` vào `data/`.
6. Chuyển `shop.log` vào `logs/`.
7. Sao chép `bai_lam.md` vào thư mục gốc dự án.
8. Giữ `.env` tại thư mục gốc và không tải file này lên GitHub.

**Lưu ý:** Cấu trúc trên thể hiện các file sau khi hoàn thành cả phần GUI và CLI. Trong phần GUI, logo và `nhap_hang.txt` vẫn ở thư mục gốc cho đến khi thực hiện phần 4.2.

## 2. Phần 4.2 – Thao tác máy tính bằng CLI

### 2.1. Bảng lệnh cơ bản

| Thao tác             | Windows PowerShell             | macOS Terminal |
| -------------------- | ------------------------------ | -------------- |
| Xem thư mục hiện tại | `Get-Location`                 | `pwd`          |
| Liệt kê nội dung     | `Get-ChildItem`                | `ls`           |
| Hiển thị file ẩn     | `Get-ChildItem -Force`         | `ls -la`       |
| Tạo thư mục          | `New-Item -ItemType Directory` | `mkdir`        |
| Di chuyển file       | `Move-Item`                    | `mv`           |
| Sao chép file        | `Copy-Item`                    | `cp`           |
| Xóa file             | `Remove-Item`                  | `rm`           |
| Chuyển thư mục       | `Set-Location`                 | `cd`           |

### 2.2. Các thao tác cần thực hiện

* Hiển thị đường dẫn tuyệt đối của thư mục hiện tại.
* Liệt kê tất cả file và thư mục, bao gồm file ẩn.
* Di chuyển `nhap_hang.txt` vào `docs/`.
* Di chuyển `logo_van_phong_pham.png` vào `media/`.
* Sao chép logo từ `media/` vào `backup/`.
* Xóa riêng file `temp_131.tmp`.
* Đi vào `logs/` bằng đường dẫn tương đối, liệt kê nội dung rồi quay lại thư mục gốc.
* Ghi các lệnh đã chạy và kết quả liệt kê toàn bộ dự án vào `bai_lam.md`.

## 3. Phần 4.3 – Lọc log thủ công

### 3.1. Mục tiêu

* Đọc file `logs/shop.log`.
* Lọc những dòng có chứa từ khóa `ERROR`.
* Ghi kết quả vào `logs/daily_report.txt`.
* Đọc lại báo cáo để kiểm tra.
* Ghi lệnh và hai dòng lỗi đầu tiên vào `bai_lam.md`.

### 3.2. Các lệnh cần ôn tập

**PowerShell:**

```powershell
Get-Content
Select-String
Set-Content
```

**macOS Terminal:**

```bash
cat
grep
```

### 3.3. Phân biệt toán tử chuyển hướng

| Toán tử | Chức năng                                 |                                             |
| ------- | ----------------------------------------- | ------------------------------------------- |
| `>`     | Ghi nội dung mới, có thể ghi đè file đích |                                             |
| `>>`    | Nối nội dung vào cuối file                |                                             |
| `       | `                                         | Chuyển kết quả của lệnh trước sang lệnh sau |

## 4. Phần 4.4 – Thao tác với tài liệu Markdown

### 4.1. Các thành phần cần có trong README.md

* Heading 1 chứa tên dự án.
* Một đoạn mô tả có cả in đậm và in nghiêng.
* Bảng `Thư mục | Nội dung` có ít nhất 3 dòng dữ liệu.
* Code block chứa lệnh PowerShell hoặc Terminal.
* Task list có ít nhất 2 công việc, trong đó có 1 công việc hoàn thành.
* Blockquote nhắc không tải `.env` lên GitHub.

### 4.2. Cú pháp Markdown cơ bản

| Thành phần                | Cú pháp                       |
| ------------------------- | ----------------------------- |
| Tiêu đề cấp 1             | `# Tiêu đề`                   |
| Tiêu đề cấp 2             | `## Tiêu đề`                  |
| In đậm                    | `**nội dung**`                |
| In nghiêng                | `*nội dung*`                  |
| Danh sách đánh số         | `1. Nội dung`                 |
| Danh sách chưa đánh số    | `- Nội dung`                  |
| Công việc hoàn thành      | `- [x] Công việc`             |
| Công việc chưa hoàn thành | `- [ ] Công việc`             |
| Blockquote                | `> Nội dung`                  |
| Code block                | Ba dấu backtick ở đầu và cuối |

## 5. Phần 4.5 – Hoàn thiện script tự động

### 5.1. Yêu cầu

Tạo script tại thư mục gốc dự án:

* Windows: `auto_report.ps1`
* macOS: `auto_report.sh`

Script cần:

1. Ghi tên tác giả và ngày tạo.
2. Đọc file `logs/shop.log`.
3. Lọc những dòng chứa `ERROR`.
4. Ghi báo cáo vào `logs/auto_report.txt`.
5. Sử dụng đường dẫn tương đối.
6. Chạy script từ thư mục gốc dự án.
7. Ghi lệnh chạy và nội dung báo cáo vào `bai_lam.md`.

### 5.2. Các kiến thức cần kiểm tra

* Cú pháp đọc file.
* Cú pháp lọc chuỗi.
* Cú pháp ghi file.
* Đường dẫn tương đối.
* Cách chạy script PowerShell hoặc shell script.

## 6. Phần 4.6 – Đếm số dòng lỗi

### 6.1. Mục tiêu

Đếm số dòng chứa `ERROR` trong `logs/shop.log` bằng pipeline.

### 6.2. Kiến thức cần nhớ

Pipeline sử dụng ký hiệu `|` để truyền kết quả từ lệnh này sang lệnh khác.

Quy trình tổng quát:

1. Đọc nội dung file log.
2. Lọc các dòng chứa `ERROR`.
3. Đếm số dòng phù hợp.
4. Ghi lệnh và kết quả đếm vào `bai_lam.md`.

## 7. Phần 4.7 – Báo cáo tổng hợp

### 7.1. Yêu cầu nội dung

Tạo file `logs/tong_hop.txt` bằng lệnh CLI, không nhập thủ công nội dung vào file.

Nội dung phải theo thứ tự:

1. Dòng đầu tiên:

   ```text
   === TONG HOP LOG ===
   ```

2. Các dòng chứa `WARNING` trong `logs/shop.log`.

3. Số dòng chứa `ERROR` trong `logs/shop.log`.

### 7.2. Các bước thực hiện

* Tạo dòng tiêu đề báo cáo.
* Đọc và lọc các dòng chứa `WARNING`.
* Đếm số dòng chứa `ERROR`.
* Kết hợp các lệnh để tạo nội dung theo đúng thứ tự.
* Đọc lại `logs/tong_hop.txt` để kiểm tra.
* Ghi các lệnh và kết quả vào `bai_lam.md`.

## 8. Phần 4.8 – Excel

### 8.1. Cấu trúc workbook

File: `data/don_ban_thang_10.xlsx`

**Sheet `SanPham`:**

| Cột | Nội dung  |
| --- | --------- |
| A   | `ma_sp`   |
| B   | `ten_sp`  |
| C   | `gia_ban` |

**Sheet `DonBan`:**

| Cột | Nội dung   |
| --- | ---------- |
| A   | `ma_db`    |
| B   | `ngay_ban` |
| C   | `ma_sp`    |
| D   | `sl_ban`   |
| E   | `ten_sp`   |
| F   | `gia_ban`  |
| G   | `tien_ban` |

### 8.2. Tra cứu tên sản phẩm

Tại ô `E2` của sheet `DonBan`, sử dụng VLOOKUP để lấy tên sản phẩm từ sheet `SanPham`.

Công thức mẫu:

```excel
=VLOOKUP(C2,SanPham!$A$2:$C$100,2,FALSE)
```

*Lưu ý: Thay dòng 100 bằng dòng cuối thực tế của bảng sản phẩm.*

### 8.3. Tra cứu giá bán

Tại ô `F2` của sheet `DonBan`, sử dụng công thức:

```excel
=VLOOKUP(C2,SanPham!$A$2:$C$100,3,FALSE)
```

Sau đó kéo công thức xuống các dòng còn lại.

### 8.4. Tính tiền bán

Tại ô `G2`, sử dụng công thức:

```excel
=D2*F2
```

Kéo công thức xuống toàn bộ các đơn bán.

**Lưu ý:** Không nhập thủ công tên sản phẩm, giá bán hoặc tiền bán thay cho công thức.

### 8.5. Lọc dữ liệu bằng AutoFilter

1. Chọn toàn bộ bảng trong sheet `DonBan`.
2. Chọn **Data → Filter**.
3. Mở bộ lọc tại cột `tien_ban`.
4. Chọn điều kiện lớn hơn hoặc bằng `300000`.
5. Xác nhận điều kiện lọc.
6. Lưu file Excel.

## 9. Kiểm tra trước khi nộp bài

* [ ] Đã chuẩn hóa tên thư mục và file.
* [ ] Đã tạo đủ 5 thư mục yêu cầu.
* [ ] Đã di chuyển và sao chép file đúng vị trí.
* [ ] Đã xóa đúng file `temp_131.tmp`.
* [ ] Đã ghi lệnh và kết quả vào `bai_lam.md`.
* [ ] Đã tạo `README.md` đúng yêu cầu.
* [ ] Đã tạo báo cáo lỗi thủ công.
* [ ] Đã hoàn thiện và chạy script tự động.
* [ ] Đã đếm số dòng lỗi bằng pipeline.
* [ ] Đã tạo báo cáo tổng hợp bằng CLI.
* [ ] Đã hoàn thiện công thức Excel và bộ lọc.
* [ ] Đã lưu file Excel.
* [ ] Không tải `.env` lên GitHub.
* [ ] Đã kiểm tra repository trước khi nộp.
* [ ] Đã gửi liên kết repository đúng hạn.

## 10. Lưu ý khi làm bài

* Thực hành trên bản sao dữ liệu để tránh mất file gốc.
* Kiểm tra thư mục hiện tại trước khi chạy lệnh di chuyển hoặc xóa.
* Sử dụng đường dẫn tương đối đúng yêu cầu.
* Không xóa hoặc tải lên các file ngoài phạm vi yêu cầu.
* Kiểm tra nội dung báo cáo sau khi tạo.
* Đảm bảo công thức Excel được kéo đầy đủ xuống các dòng dữ liệu.
* Giữ nguyên cấu trúc thư mục theo yêu cầu của đề thi.
