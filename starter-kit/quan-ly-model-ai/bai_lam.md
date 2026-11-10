# mini-project
- **Mã đề:** 
- **Họ tên:** Đào Tuấn Minh
- **Lớp:** CNTT3
- **Link repository:**
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```Powershell
1.PS D:\starter-kit\quan-ly-model-ai> pwd
2.PS D:\starter-kit\quan-ly-model-ai> ls -Force
3.PS D:\starter-kit\quan-ly-model-ai> mv .\chi_phi_model_thang_11.xlsx .\data
4.PS D:\starter-kit\quan-ly-model-ai> mkdir backup
5.PS D:\starter-kit\quan-ly-model-ai> cp .\data\chi_phi_model_thang_11.xlsx .\backup
6.PS D:\starter-kit\quan-ly-model-ai> rm .\model_cache_01.tmp
7.PS D:\starter-kit\quan-ly-model-ai> cd .\logs
8.PS D:\starter-kit\quan-ly-model-ai\logs> ls
9.PS D:\starter-kit\quan-ly-model-ai\logs> cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
   Directory: D:\starter-kit\quan-ly-model-ai
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/10/2026   1:49 PM                data
d-----        11/10/2026   1:46 PM                docs
d-----        11/10/2026   1:46 PM                evidence
d-----        11/10/2026   1:49 PM                logs
d-----        11/10/2026   1:44 PM                web
-a----        11/10/2026   1:43 PM             96 .env
-a----        11/10/2026   1:43 PM           2665 bai_lam.md
-a----        11/10/2026   1:43 PM           5815 chi_phi_model_thang_11.xlsx
-a----        11/10/2026   1:43 PM           1234 inference.log
-a----        11/10/2026   1:43 PM             44 model_cache_01.tmp
-a----        11/10/2026   1:43 PM            204 tai_lieu_ban_giao.txt
```

## 4.3. Lọc log vận hành Model AI

### a) Lệnh lọc các dòng WARNING

```Powershell
PS D:\starter-kit\quan-ly-model-ai> Get-Content ".\logs\inference.log" | Select-String "WARNING" >> .\logs\loi_model.txt```

### 2 dòng đầu tiên trong logs/loi_error.txt

```text
2026-11-10 08:09:18 WARNING POST /v1/embeddings model=LLAMA-2-OLD
2026-11-10 08:16:05 WARNING GET /v1/fine-tune/jobs-legacy
```

### b) Lệnh đếm số dòng ERROR và kết quả

```Powershell
PS D:\starter-kit\quan-ly-model-ai> (Get-Content ".\logs\inference.log" | Select-String "ERROR").count >> .\logs\loi_model.txt
```

```text
6
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```Powershell
1.PS D:\starter-kit\quan-ly-model-ai> Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
2.PS D:\starter-kit\quan-ly-model-ai> .\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO VAN HANH MODEL AI ===

2026-11-10 08:09:18 WARNING POST /v1/embeddings model=LLAMA-2-OLD
2026-11-10 08:16:05 WARNING GET /v1/fine-tune/jobs-legacy
2026-11-10 08:38:29 WARNING GET /images/model-card-v1.png
2026-11-10 09:01:44 WARNING POST /v1/completions model=DAVINCI-002
2026-11-10 09:14:02 WARNING GET /v1/quota/expired-key

6
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và _in nghiêng_, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |                            |                             |                |
| 2   |                            |                             |                |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:**
- **Expected:**
- **Actual:**
- **Log:**

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_11.xlsx`, không cần ghi vào đây.

