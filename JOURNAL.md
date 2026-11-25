# Nhật ký phát triển

Ghi lại quyết định, khó khăn và bài học trong quá trình phát triển. Công việc chi tiết theo ngày xem [WORKLOG.md](WORKLOG.md).

## 2026-10-15

- Bỏ polling định kỳ gây nháy ở chat/ticket và bảng cán bộ/admin; giữ thao tác làm mới thủ công.
- Sửa breakpoint mobile bị stylesheet tải sau ghi đè; đặt cỡ chữ input tối thiểu 16px trên mobile để tránh Safari tự zoom khi focus.
- Bổ sung email thông báo sau khi lưu phản hồi, lưu trạng thái gửi riêng, chỉ dùng email tài khoản đã xác minh và thêm gửi lại khi lỗi.
- Tạo nút vào demo cán bộ/admin cho `development`/`test`; API demo bị tắt trong `production`.
- Giới hạn: tác vụ email nền dùng FastAPI BackgroundTasks, chưa có hàng đợi bền vững.
