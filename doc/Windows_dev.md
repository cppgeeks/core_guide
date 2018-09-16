# Phát triển trên Windows

## 1. Cài đặt package manager
- Sử dụng CMD hoặc PowerShell
- Nên dùng CMD vì đơn giản và chạy nhanh hơn
- Tuy nhiên PowerShell rất mạnh mẽ và cần thiết nếu chuyên Windows
- Mở CMD với quyền admin (chuột phải Run As Administrator)
- https://chocolatey.org/docs/installation

## 2. Cài đặt các công cụ cần thiết
- Sử dụng lệnh `choco install`
- Thêm `-y` để tự động chấp nhận câu hỏi về thỏa thuận cài đặt
- Sau khi cài đặt dùng lệnh `refreshenv` để sử dụng ứng dụng đã cài <br />
CMD sẽ đọc lại biến môi trường Path
- Cài đặt: cmake, msys2
- Ví dụ: <br />
`choco install -y cmake` <br />
`refresh env` <br />
`cmake --version`

## 3. MSYS2
- Lệnh `pacman -Ss tên_package` để tìm kiếm
- Lệnh `pacman -S tên_package` để cài đặt
- Lệnh `pacman -R tên_package` để gỡ cài đặt
- Chỉ sử dụng các package dành cho MinGW64 (64-bit)
- Ví dụ: <br />
`choco install -y msys2` <br />
`refreshenv` <br />
`mingw64` <br />
chuyển qua shell MinGW64 gõ: <br />
`pacman -Ss gcc` <br />
`pacman -S mingw-w64-x86_64-gcc`
- Cài thêm các package sau: `mingw32-make`
- Copy `mingw32-make.exe` thành `make.exe` để chạy `Makefile`: <br />
`which mingw32-make` <br />
`cp output_của_lệnh_trên output_của_lệnh_trên_thay_mingw32-make_thành_make`

## 4. Sử dụng công cụ của MSYS2 trong CMD
- Thay vì phải vào `mingw64 shell` gõ lệnh, có thể gõ trong `CMD`
- Thêm đường dẫn của thư mục bin (mingw64) vào biến môi trường Path
- Kiểm tra trên CMD: <br />
`cmake --version` <br />
`g++ -v` <br />
`make -v`

