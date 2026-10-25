# Báo Cáo Thực Hành Git & GitHub

Kho lưu trữ ghi lại toàn bộ tiến trình thực hành 41 bài tập Git và GitHub, bao gồm các thao tác từ cơ bản, làm việc nhóm, xử lý phân nhánh, phục hồi dữ liệu đến tự động hóa.

## 1. Mục đích
- Nắm vững quy trình quản lý phiên bản mã nguồn cục bộ với Git.
- Thành thạo tương tác và làm việc cộng tác với remote repository trên nền tảng GitHub.
- Xử lý các tình huống nâng cao: giải quyết xung đột mã nguồn, phân tích lỗi, khôi phục trạng thái commit và tự động hóa quy trình kiểm thử trước khi commit.

## 2. Hướng dẫn sử dụng kho lưu trữ

### Sao chép kho lưu trữ về máy (Clone kèm Submodule)
git clone --recurse-submodules https://github.com/HoThuann/ThucHanhGit_HoMyThuan.git
cd ThucHanhGit_HoMyThuan

# Báo Cáo Thực Hành Git & GitHub

Kho lưu trữ ghi lại toàn bộ tiến trình thực hành 41 bài tập Git và GitHub, bao gồm các thao tác từ cơ bản, làm việc nhóm, xử lý phân nhánh, phục hồi dữ liệu đến tự động hóa.

## 1. Mục đích
- Nắm vững quy trình quản lý phiên bản mã nguồn cục bộ với Git.
- Thành thạo tương tác và làm việc cộng tác với remote repository trên nền tảng GitHub.
- Xử lý các tình huống nâng cao: giải quyết xung đột mã nguồn, phân tích lỗi, khôi phục trạng thái commit và tự động hóa quy trình kiểm thử trước khi commit.

## 2. Hướng dẫn sử dụng kho lưu trữ

### Sao chép kho lưu trữ về máy (Clone kèm Submodule)
git clone --recurse-submodules https://github.com/HoThuann/ThucHanhGit_HoMyThuan.git
cd ThucHanhGit_HoMyThuan

### Kiểm tra lịch sử và trạng thái
git status
git log --oneline --graph --all

## 3. Các kỹ thuật đã thực hiện

### Cơ bản và Vùng làm việc (Working Tree, Index, Commit)
- Cấu hình thông tin người dùng (git config), khởi tạo kho lưu trữ (git init), đưa tệp vào khu vực theo dõi (git add) và tạo phiên bản lưu trữ (git commit).
- Xem sự khác biệt giữa các trạng thái tệp (git diff) và hủy bỏ chỉnh sửa chưa stage/đã stage (git restore).
- Loại trừ tệp tạm, tệp nhật ký không cần theo dõi bằng .gitignore.

### Nhánh, Hợp nhất và Xung đột (Branch, Merge, Rebase)
- Tạo nhánh, chuyển đổi nhánh (git checkout -b, git switch).
- Thực hiện ghép nhánh không chuyển hướng (fast-forward) và ghép nhánh tạo điểm nối (3-way merge commit).
- Chủ động phát hiện và giải quyết xung đột mã nguồn (merge conflict) thủ công.
- Tái cấu trúc lịch sử commit bằng git rebase và gắn nhãn phiên bản phát hành (git tag v1.0.0).

### Tương tác GitHub và Làm việc nhóm
- Kết nối remote repository qua giao thức HTTPS và xác thực khóa SSH an toàn.
- Đẩy dữ liệu (git push), kéo dữ liệu (git pull) và cấu hình nhiều nguồn từ xa (origin, upstream).
- Tạo và sáp nhập yêu cầu kéo (Pull Request) trên giao diện GitHub.
- Xuất bản trang web tĩnh trực tiếp qua GitHub Pages.

### Phục hồi và Truy vết (Inspection & Recovery)
- Gỡ bỏ tệp khỏi Git nhưng vẫn giữ tệp cục bộ (git rm --cached).
- Truy xuất nội dung tệp ở commit quá khứ (git show) và xem lịch sử riêng của một tệp (git log -- file).
- Tìm kiếm chuỗi văn bản trong toàn bộ mã nguồn được theo dõi bằng git grep.
- Áp dụng thuật toán tìm kiếm nhị phân git bisect để dò tìm chính xác commit đầu tiên gây ra lỗi hệ thống.
- Cứu các commit và dữ liệu bị xóa nhầm do reset nhầm bằng git reflog.
- Hoàn tác an toàn các commit đã đẩy lên máy chủ bằng git revert.

### Kỹ thuật nâng cao và Tự động hóa
- Lưu tạm công việc dở dang bằng ngăn xếp git stash để xử lý tác vụ khẩn cấp.
- Thiết lập phím tắt lệnh (git alias) tăng tốc độ thao tác terminal.
- Tích hợp kho mã nguồn con độc lập vào dự án thông qua git submodule.
- Viết script pre-commit hook tự động kiểm tra cú pháp và chặn các commit chứa từ khóa cấm.
