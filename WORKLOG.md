# Worklog

Ghi lại công việc theo ngày: làm gì, kết quả ra sao.

## 2026-10-10 — QA vòng 2 trên production

- **Việc:** QA production cho Trợ lý tuyển sinh X; xử lý ticket QA_TEST; lập ma trận AI, test case, báo cáo UI/data/security/E2E.
- **Kết quả:** Hoàn thành audit, không sửa mã sản phẩm. Kết luận NO-GO do thiếu độ phủ và full suite còn 1 test đỏ. E2E cán bộ/admin đã xác nhận phản hồi và trạng thái; chưa xác minh được phiên thí sinh sở hữu ticket.
- **Output:** `qa-reports/round-2/ROUND2_EXECUTIVE_SUMMARY.md`
- **Tổng kết:** 52 ca chức năng (26 PASS, 3 PARTIAL, 1 BLOCKED, 2 FAIL, 20 NOT_TESTED) và 150 câu AI, trong đó 145 câu chưa chạy.

## 2026-10-15 — Email thông báo, responsive, lối vào demo

- **Việc:** Gỡ tự làm mới định kỳ; sửa responsive mobile; thêm email thông báo an toàn sau khi cán bộ phản hồi ticket; mở lối vào demo cán bộ/admin cho môi trường dev/test; thêm kiểm thử và tài liệu.
- **Kết quả:** Hoàn tất mã; kiểm tra tĩnh và 3 test đơn vị PASS. Test HTTP dừng ở fixture `AsyncClient`.
- **Output:** `src/web/app.js`, `src/web/staff.js`, `src/web/admin.js`, `src/api/routes.py`, `src/services/store.py`, `src/services/email.py`, `tests/test_api/test_mvp.py`, `README-MVP.md`
- **Tổng kết:** Email dùng chung Resend/SMTP hiện có; kiểm thử chỉ dùng mailer giả, không gửi thư thật. Test mẫu email, outbox/retry và production guard đã PASS; Ruff và compileall sạch.
