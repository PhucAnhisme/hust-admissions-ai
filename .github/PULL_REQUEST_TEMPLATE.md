## Thay đổi gì

<!-- Mô tả ngắn gọn thay đổi và lý do. -->

## Loại thay đổi

- [ ] `fix` — sửa lỗi
- [ ] `feat` — tính năng mới
- [ ] `docs` — tài liệu
- [ ] `data` — nguồn tuyển sinh / bộ đánh giá
- [ ] `chore` / `refactor` / `test`

## Checklist

- [ ] `ruff check src tests` sạch
- [ ] `pytest` xanh
- [ ] Nếu đổi logic trả lời hoặc dữ liệu: đã chạy `python -m scripts.evaluate_mvp --suite golden`
- [ ] **Không có API key / token / credential** trong diff (kể cả `.env.example`)
