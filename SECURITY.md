# Chính sách bảo mật

## Báo cáo lỗ hổng

**Không** mở public issue cho lỗ hổng bảo mật.

Dùng [GitHub Security Advisories](https://github.com/PhucAnhisme/hust-admissions-ai/security/advisories/new) để báo cáo riêng tư. Vui lòng mô tả loại lỗ hổng, file/dòng liên quan, các bước tái hiện và tác động bạn đánh giá.

## Nếu bạn lỡ commit một API key

Xoá key khỏi file rồi commit tiếp là **chưa đủ**: giá trị cũ vẫn nằm trong git history và trong mọi bản clone/fork. Coi như key đã lộ hoàn toàn.

1. **Xoay key ngay (rotate).** Đây là bước duy nhất thật sự vô hiệu hoá key cũ.
2. Thay bằng placeholder trong file rồi commit.
3. Nếu cần xoá khỏi history, dùng [git-filter-repo](https://github.com/newren/git-filter-repo) rồi force-push.

## Lưu ý khi triển khai

- Không đặt key thật vào `.env.example`; key thật chỉ nằm trong `.env` hoặc secret manager của nền tảng deploy.
- Ở production, đặt `APP_ENV=production`, `SECURE_COOKIES=true`, `AUTH_SECRET` ngẫu nhiên ≥ 32 ký tự và đổi mọi mật khẩu demo. App từ chối khởi động nếu vẫn dùng mật khẩu demo.
- Database SQLite chứa tài khoản, ticket và hội thoại của ứng viên; không đưa vào Git, không gửi kèm khi bàn giao.
- Kiểm tra nhanh trước khi push:
  ```bash
  git diff --cached | grep -iE "api[_-]?key|secret|token|password"
  ```
