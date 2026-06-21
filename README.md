Xây dựng chương trình thi trắc nghiệm chạy trên giao diện console bằng ngôn ngữ C++. Chương trình hỗ trợ quản lý môn học, ngân hàng câu hỏi, thí sinh, tổ chức bài thi, chấm điểm và lưu kết quả vào file văn bản.

## Chức năng chính

- Quản lý danh sách môn học.
- Quản lý ngân hàng câu hỏi trắc nghiệm.
- Quản lý thông tin thí sinh.
- Tạo đề thi ngẫu nhiên theo môn học và loại câu hỏi.
- Thực hiện bài thi trên giao diện console.
- Tự động chấm điểm sau khi hoàn thành bài thi.
- Lưu và đọc dữ liệu từ các file văn bản.
- Tra cứu, thống kê và xuất báo cáo kết quả thi.

## Cấu trúc dự án

```text
KTLT_project/
├── .vscode/
│   └── tasks.json
├── data/
│   ├── candidates.txt
│   ├── questions.txt
│   ├── results.txt
│   └── subjects.txt
├── bao_cao.cpp
├── bao_cao.h
├── du_lieu.cpp
├── du_lieu.h
├── main.cpp
├── menu.cpp
├── menu.h
├── ngan_hang_cau_hoi.cpp
├── ngan_hang_cau_hoi.h
├── thi.cpp
├── thi.h
├── tien_ich.cpp
├── tien_ich.h
├── test.cpp
├── build_and_run.bat
└── README.md
```

## Vai trò của các module

| Module | Chức năng |
|---|---|
| `main.cpp` | Điểm bắt đầu của chương trình |
| `menu.cpp`, `menu.h` | Hiển thị menu và điều hướng chức năng |
| `du_lieu.cpp`, `du_lieu.h` | Đọc, ghi và xử lý dữ liệu từ file |
| `ngan_hang_cau_hoi.cpp`, `ngan_hang_cau_hoi.h` | Quản lý câu hỏi và tạo đề thi |
| `thi.cpp`, `thi.h` | Tổ chức quá trình thi và chấm điểm |
| `bao_cao.cpp`, `bao_cao.h` | Thống kê và hiển thị báo cáo |
| `tien_ich.cpp`, `tien_ich.h` | Các hàm tiện ích dùng chung |
| `test.cpp` | Kiểm thử một số chức năng của chương trình |
| `data/` | Lưu dữ liệu lâu dài của hệ thống |

## Dữ liệu của chương trình

Chương trình sử dụng các file văn bản trong thư mục `data`:

- `subjects.txt`: danh sách môn học.
- `questions.txt`: ngân hàng câu hỏi.
- `candidates.txt`: thông tin thí sinh.
- `results.txt`: kết quả các bài thi.

Khi khởi động, chương trình đọc dữ liệu từ các file trên vào bộ nhớ. Khi dữ liệu thay đổi hoặc có kết quả thi mới, chương trình ghi lại dữ liệu vào file tương ứng.

## Cách chạy chương trình

### Cách 1: Sử dụng file có sẵn

Chạy file:

```bat
build_and_run.bat
```

Có thể nhấp đúp vào file hoặc chạy trong Terminal của Visual Studio Code:

```powershell
.\build_and_run.bat
```

### Cách 2: Biên dịch thủ công

Mở Terminal tại thư mục dự án và chạy:

```bash
g++ -std=c++17 main.cpp menu.cpp du_lieu.cpp ngan_hang_cau_hoi.cpp thi.cpp bao_cao.cpp tien_ich.cpp -o KTLT_project.exe
```

Sau đó chạy chương trình:

```powershell
.\KTLT_project.exe
```

## Quy trình hoạt động

1. Chương trình đọc dữ liệu từ thư mục `data`.
2. Người dùng chọn chức năng trên menu chính.
3. Hệ thống xử lý môn học, câu hỏi, thí sinh hoặc bài thi.
4. Khi thi, chương trình chọn câu hỏi và tạo đề.
5. Thí sinh nhập đáp án trực tiếp trên console.
6. Hệ thống chấm điểm và lưu kết quả vào `data/results.txt`.
7. Người dùng có thể xem lại hoặc thống kê kết quả thi.

## Một số kỹ thuật sử dụng

- Chia chương trình thành các file `.h` và `.cpp`.
- Sử dụng hàm và module để tách biệt từng nhóm chức năng.
- Sử dụng mảng hoặc `vector` để quản lý dữ liệu trong bộ nhớ.
- Đọc và ghi file văn bản để lưu dữ liệu lâu dài.
- Lập trình phòng ngừa
- Đặt tên biến
- Chú thích và quy tắc lập trình
- Lập trình có cấu trúc
- Sinh số ngẫu nhiên để trộn hoặc lựa chọn câu hỏi.
- Tìm kiếm, lọc, đếm và thống kê dữ liệu.
