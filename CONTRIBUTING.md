# Đóng góp cho HUST Admissions AI

Đây là dự án cá nhân. Mọi góp ý, báo lỗi hay pull request đều được hoan nghênh.

## Quy trình

1. Fork repo, tạo nhánh từ `main`, ví dụ `git checkout -b fix/hoc-phi-it1`.
2. Commit theo [Conventional Commits](https://www.conventionalcommits.org/):
   `feat:`, `fix:`, `docs:`, `chore:`, `test:`, `refactor:`.
3. Chạy kiểm tra trước khi push:
   ```bash
   ruff check src tests
   pytest -q
   ```
4. Nếu thay đổi logic trả lời hoặc dữ liệu nguồn, chạy thêm bộ đánh giá (không gọi API):
   ```bash
   python -m scripts.evaluate_mvp --suite golden --retrieval bm25
   ```
5. Mở PR vào `main`. CI ([.github/workflows/ci.yml](.github/workflows/ci.yml)) phải xanh.

## Dữ liệu tuyển sinh

- Chỉ thêm nguồn công khai, ghi rõ URL, năm áp dụng và ngày truy cập trong `data/sources.md`.
- Không sửa nhãn trong `eval/` chỉ để khớp với output hiện tại của hệ thống.
- Không commit dữ liệu hội thoại hay thông tin cá nhân của ứng viên.

## Không commit thông tin bí mật

Không commit API key, token, mật khẩu hay credential, kể cả trong `.env.example`, comment hay tài liệu.

- `.env.example` chỉ chứa placeholder.
- Giá trị thật đặt trong `.env`; file này đã nằm trong `.gitignore`.
- Nếu lỡ commit, xem [SECURITY.md](SECURITY.md): key coi như đã lộ và **phải được xoay (rotate)**.

## Báo lỗi

Mở [issue](https://github.com/PhucAnhisme/hust-admissions-ai/issues) kèm môi trường (OS, phiên bản Python), các bước tái hiện và log lỗi.

Lỗ hổng bảo mật thì **không** mở issue công khai; làm theo [SECURITY.md](SECURITY.md).

## Quy tắc ứng xử

Tham gia dự án đồng nghĩa với việc bạn đồng ý tuân thủ [Quy tắc ứng xử](CODE_OF_CONDUCT.md).
