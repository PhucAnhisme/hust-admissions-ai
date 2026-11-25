# TỔNG QUAN NỘI DUNG DỰ ÁN
## HỆ THỐNG TRỢ LÝ TUYỂN SINH THÔNG MINH · ĐẠI HỌC BÁCH KHOA HÀ NỘI (HUST 2026)

---

## 1. BỐI CẢNH VÀ MỤC TIÊU DỰ ÁN

### 1.1. Bối Cảnh Thực Tế
Đại học Bách khoa Hà Nội là một trong những cơ sở giáo dục đại học kỹ thuật trọng điểm hàng đầu cả nước. Mỗi mùa tuyển sinh, Nhà trường thu hút hàng chục nghìn thí sinh trên toàn quốc tham gia xét tuyển với nhu cầu thông tin rất lớn:
* **Hệ thống phương thức xét tuyển đa dạng và chuyên sâu:** Xét tuyển tài năng (XTTN), Đánh giá tư duy (TSA), Xét theo kết quả thi tốt nghiệp THPT, cùng các quy định phức tạp về chứng chỉ ngoại ngữ quốc tế (IELTS, TOEFL, V-SAT...).
* **Quy mô đào tạo lớn:** Gần 70 chương trình đào tạo thuộc nhiều hệ (Chương trình chuẩn, Chương trình tiên tiến ELITECH, Chương trình liên kết quốc tế) với mức học phí, chỉ tiêu và tiêu chuẩn đầu ra khác nhau.
* **Tài liệu đề án dài và chi tiết:** Bản Đề án tuyển sinh chính thức dài hơn 50 trang văn bản pháp lý, khiến thí sinh và phụ huynh gặp nhiều khó khăn khi tự tra cứu, dễ dẫn đến hiểu nhầm điều kiện nộp hồ sơ.
* **Tình trạng quá tải tư vấn:** Các kênh truyền thống (Hotline, Fanpage, Email) luôn chịu áp lực lớn trong giai đoạn cao điểm, khó phản hồi kịp thời và dễ phát sinh sai sót do trả lời thủ công.

### 1.2. Mục Tiêu Dự Án
Dự án được xây dựng nhằm tạo ra một giải pháp số hóa toàn diện cho công tác tuyển sinh:
* **Tự động hóa tư vấn 24/7:** Phản hồi ngay lập tức mọi câu hỏi của thí sinh và phụ huynh với tốc độ dưới 1 giây.
* **Chính xác tuyệt đối và loại bỏ hoàn toàn "ảo giác" (Zero Hallucination):** Câu trả lời phải bám sát từng câu chữ của Đề án tuyển sinh chính thức, không tự suy đoán thông tin ngoài văn bản.
* **Minh bạch nguồn gốc:** Mọi phản hồi đều trích dẫn chính xác số trang tài liệu để người hỏi tự kiểm chứng.
* **Khép kín luồng xử lý:** Khi gặp các trường hợp cá biệt nằm ngoài văn bản, hệ thống tự động chuyển tiếp câu hỏi tới cán bộ tuyển sinh để giải quyết dứt điểm 100% thắc mắc.

---

## 2. NỘI DUNG VÀ CÁC PHÂN HỆ NGHIỆP VỤ CHÍNH

Hệ thống được thiết kế thành 4 khối nghiệp vụ cốt lõi, phục vụ đồng thời thí sinh, phụ huynh và đội ngũ tuyển sinh của Nhà trường:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        HỆ THỐNG TRỢ LÝ TUYỂN SINH                      │
└────────────────────────────────────────────────────────────────────────┘
       │                                                   │
       ▼                                                   ▼
┌──────────────────────────────┐        ┌────────────────────────────────┐
│   DÀNH CHO NGƯỜI DÙNG        │        │   DÀNH CHO NHÀ TRƯỜNG          │
├──────────────────────────────┤        ├────────────────────────────────┤
│ 1. Hỏi đáp RAG kiểm chứng    │        │ 3. Cổng Cán bộ tiếp nhận       │
│    - Quy chế, mốc thời gian  │        │    - Xử lý câu hỏi khó/ngoại lệ│
│    - Điều kiện & tổ hợp môn  │        │    - Soạn câu trả lời xác thực │
│    - Dẫn chứng số trang PDF  │        │    - Gửi email phản hồi        │
│                              │        │                                │
│ 2. Tra cứu & So sánh ngành   │        │ 4. Quản trị & Giám sát         │
│    - Ghim ngữ cảnh ngành     │        │    - Thống kê xu hướng hỏi     │
│    - So sánh chỉ tiêu/học phí│        │    - Đánh giá chất lượng RAG   │
│    - Điểm chuẩn các năm      │        │    - Quản lý cấu hình & quyền  │
└──────────────────────────────┘        └────────────────────────────────┘
```

---

### 2.1. Phân Hệ Hỏi Đáp & Truy Xuất Kiến Thức Đề Án
* **Nội dung tư vấn:**
  - Hướng dẫn điều kiện nộp hồ sơ của từng phương thức xét tuyển (Xét tuyển tài năng theo giải thưởng học sinh giỏi/chứng chỉ quốc tế; Xét tuyển theo điểm thi Đánh giá tư duy; Xét tuyển theo điểm thi Tốt nghiệp THPT).
  - Quy định quy đổi điểm thưởng, cách cộng điểm ưu tiên khu vực/đối tượng và bảng quy đổi chứng chỉ tiếng Anh (IELTS, TOEIC...).
  - Các mốc thời gian đăng ký nguyện vọng, nộp hồ sơ trực tuyến, đóng lệ phí xét tuyển và công bố kết quả.
  - Thông tin học phí dự kiến từng học kỳ, chính sách học bổng khuyến khích tài năng, học bổng doanh nghiệp và chính sách miễn giảm học phí.
* **Cơ chế kiểm soát chất lượng:**
  - Áp dụng cơ chế tìm kiếm kết hợp (Hybrid Search) giữa từ khóa chính xác và ngữ nghĩa ngôn ngữ tự nhiên để hiểu câu hỏi linh hoạt nhưng vẫn bắt đúng thuật ngữ tuyển sinh.
  - Tích hợp cổng kiểm chứng độc lập (Grounding Gate) kiểm tra câu trả lời trước khi gửi tới người dùng. Nếu thông tin không có căn cứ từ văn bản chính thức, hệ thống sẽ từ chối khẳng định và hướng dẫn thí sinh hỏi cán bộ tư vấn.

---

### 2.2. Phân Hệ Tra Cứu & Đối Chiếu 68 Chương Trình Đào Tạo
* **Nội dung phục vụ:**
  - Cung cấp danh mục toàn bộ gần 70 chương trình đào tạo của Đại học Bách khoa Hà Nội với mã ngành chuẩn hóa.
  - Phân loại rõ ràng giữa các hệ đào tạo: Chương trình chuẩn (giảng dạy tiếng Việt), Chương trình tiên tiến ELITECH (học chuyên sâu, tăng cường ngoại ngữ) và Chương trình đào tạo quốc tế liên kết với các trường đại học nước ngoài.
* **Tính năng hỗ trợ thí sinh:**
  - **Ghim ngữ cảnh tra cứu:** Cho phép người dùng chọn đích danh mã ngành muốn hỏi (ví dụ: chỉ hỏi ngành Khoa học Máy tính hoặc Kỹ thuật Cơ điện tử). Trợ lý sẽ tập trung dữ liệu vào đúng ngành đó, tránh việc thông tin của ngành này bị trộn lẫn sang ngành khác.
  - **Thẻ so sánh đa chiều:** Đặt các ngành phân vân lên bàn cân so sánh song song theo các chỉ số quan trọng: Chỉ tiêu tuyển sinh từng phương thức, tổ hợp xét tuyển, điểm chuẩn 3 năm gần nhất và mức học phí dự kiến, giúp thí sinh đưa ra quyết định đặt thứ tự nguyện vọng 1, nguyện vọng 2 hợp lý nhất.

---

### 2.3. Phân Hệ Điều Phối Hỗ Trợ Chuyên Sâu (Cổng Cán Bộ Tuyển Sinh)
* **Nội dung phục vụ:**
  - Tiếp nhận những trường hợp cá biệt: thí sinh thuộc diện chính sách đặc biệt, thí sinh tự do, trường hợp thiếu giấy tờ chứng minh, thí sinh có giải thưởng quốc tế cần tham vấn hội đồng tuyển sinh.
* **Quy trình hoạt động:**
  - **Tự động nhận diện ngoại lệ:** Khi câu hỏi vượt quá phạm vi văn bản Đề án hoặc khi thí sinh chủ động bấm nút yêu cầu hỗ trợ chuyên sâu, hệ thống tự động ghi nhận họ tên, email, số điện thoại và toàn bộ lịch sử trao đổi vào một "Phiếu tư vấn" (Ticket).
  - **Giao diện Cán bộ Tuyển sinh:** Thầy cô phụ trách tuyển sinh đăng nhập vào cổng làm việc riêng, xem danh sách phiếu chờ xử lý, xem toàn bộ lịch sử trao đổi của thí sinh để nắm rõ ngữ cảnh mà không cần hỏi lại từ đầu.
  - **Phản hồi chính thức qua Email:** Cán bộ soạn thảo câu trả lời và phê duyệt gửi thư xác thực từ hòm thư tuyển sinh chính thức của Nhà trường đến email của thí sinh.

---

### 2.4. Phân Hệ Quản Trị & Giám Sát Vận Hành
* **Nội dung phục vụ:**
  - Giúp Ban Quản trị và Hội đồng Tuyển sinh theo dõi toàn bộ trạng thái hoạt động của hệ thống theo thời gian thực.
* **Các tính năng giám sát:**
  - **Thống kê xu hướng tuyển sinh:** Đo lường các chủ đề, các ngành đào tạo và các phương thức xét tuyển đang nhận được sự quan tâm nhiều nhất từ xã hội.
  - **Giám sát độ tin cậy của AI:** Ghi nhận vết (Trace) của từng lượt hội thoại, đo lường độ trễ phản hồi, tỷ lệ câu hỏi được giải quyết tự động và tỷ lệ câu hỏi phải chuyển tiếp cho cán bộ.
  - **Bảo mật và phân quyền:** Đảm bảo dữ liệu liên hệ của thí sinh được bảo mật tuyệt đối, phân định quyền truy cập rõ ràng giữa các tài khoản cán bộ và quản trị viên.

---

## 3. KIẾN TRÚC VẬN HÀNH & CÁC LUỒNG HOẠT ĐỘNG CHÍNH

Hệ thống được tổ chức thành **4 tầng kỹ thuật phân tách rõ ràng**, vận hành nhịp nhàng qua 3 luồng công việc chính:

### 3.1. Bốn Tầng Kiến Trúc Hệ Thống

```
┌────────────────────────────────────────────────────────────────────────┐
│ TẦNG 1: GIAO DIỆN & TƯƠNG TÁC (Web Chat, Cổng Cán Bộ, Trang Quản Trị)  │
└────────────────────────────────────┬───────────────────────────────────┘
                                     │ Kết nối thời gian thực (SSE)
┌────────────────────────────────────▼───────────────────────────────────┐
│ TẦNG 2: CỔNG ĐIỀU PHỐI DỊCH VỤ (Tiếp nhận & Định tuyến yêu cầu)        │
└────────────────────────────────────┬───────────────────────────────────┘
                                     │
┌────────────────────────────────────▼───────────────────────────────────┐
│ TẦNG 3: BỘ NÃO AI & XỬ LÝ DỮ LIỆU (Hybrid RAG & Kiểm chứng Grounding)  │
└────────────────────────────────────┬───────────────────────────────────┘
                                     │
┌────────────────────────────────────▼───────────────────────────────────┐
│ TẦNG 4: KHO TRI THỨC GỐC (51 Trang Đề án K71, 68 Ngành, Phiếu Tư Vấn) │
└────────────────────────────────────────────────────────────────────────┘
```

1. **Tầng Giao Diện & Tương Tác:** Cung cấp trải nghiệm trò chuyện mượt mà trên nền tảng web, hỗ trợ hiển thị phản hồi tức thì từng từ (streaming), khung chọn mã ngành tiện lợi và các bảng thông số trực quan.
2. **Tầng Cổng Điều Phối Dịch Vụ:** Tiếp nhận toàn bộ yêu cầu từ người dùng, quản lý phiên làm việc, phân loại yêu cầu là tra cứu thông tin, so sánh ngành hay tạo phiếu hỗ trợ gửi cán bộ.
3. **Tầng Bộ Não AI & Xử Lý Dữ Liệu:** Trực tiếp phân tích ý định câu hỏi, kích hoạt tìm kiếm kép trên tài liệu, lọc lại các đoạn văn bản phù hợp nhất và chạy bộ lọc chống ảo giác để bảo đảm độ chính xác.
4. **Tầng Kho Tri Thức Gốc:** Lưu trữ toàn bộ 51 trang văn bản Đề án tuyển sinh K71, kho dữ liệu thông số gần 70 chương trình đào tạo và cơ sở dữ liệu quản lý các phiếu tư vấn.

---

### 3.2. Ba Luồng Hoạt Động Cốt Lõi Của Hệ Thống

#### Luồng 1: Hỏi Đáp Nhanh & Kiểm Chứng Nguồn Gốc (Thời gian < 1 giây)
* **Bước 1:** Thí sinh nhập câu hỏi về quy chế, phương thức xét tuyển hoặc điểm chuẩn.
* **Bước 2:** Hệ thống tự động phân loại ý định và tìm kiếm đồng thời theo từ khóa và theo ngữ nghĩa trên toàn bộ nội dung Đề án tuyển sinh.
* **Bước 3:** Cổng kiểm chứng độc lập rà soát câu trả lời với các đoạn trích từ văn bản gốc, loại bỏ hoàn toàn các thông tin suy diễn không có căn cứ.
* **Bước 4:** Câu trả lời xuất hiện trên màn hình kèm theo nhãn số trang tài liệu chính thức (ví dụ: *📄 Đề án K71 · Trang 18*). Thí sinh có thể bấm vào để xem ngay trang tài liệu gốc.

#### Luồng 2: Tra Cứu & Đối Chiếu Các Chương Trình Đào Tạo
* **Bước 1:** Thí sinh lựa chọn các ngành muốn cân nhắc (ví dụ: Công nghệ thông tin chuẩn và Công nghệ thông tin Global ICT).
* **Bước 2:** Hệ thống trích xuất dữ liệu có cấu trúc từ kho dữ liệu tuyển sinh của Nhà trường mà không thông qua suy đoán tự do của AI, bảo đảm số liệu chuẩn xác 100%.
* **Bước 3:** Tự động đối chiếu các chỉ số: chỉ tiêu, tổ hợp môn thi, mức học phí và cơ hội nghề nghiệp.
* **Bước 4:** Kết quả hiển thị dưới dạng thẻ đối chiếu trực quan, giúp thí sinh dễ dàng chọn được ngành phù hợp nhất với năng lực và điều kiện cá nhân.

#### Luồng 3: Xử Lý Ngoại Lệ & Hỗ Trợ Chuyên Sâu Từ Cán Bộ
* **Bước 1:** Phát hiện các câu hỏi đặc thù vượt ngoài văn bản hoặc khi thí sinh cần tư vấn trực tiếp từ thầy cô.
* **Bước 2:** Hệ thống tạo Phiếu tư vấn (Ticket), cấp mã tra cứu riêng và lưu giữ lại toàn bộ lịch sử câu hỏi của thí sinh.
* **Bước 3:** Cán bộ tuyển sinh tiếp nhận phiếu tại cổng làm việc, xem xét hồ sơ và soạn nội dung giải đáp chính thức.
* **Bước 4:** Phản hồi được gửi trực tiếp đến hộp thư điện tử của thí sinh, đảm bảo giá trị pháp lý và không bỏ sót bất kỳ thắc mắc nào trong mùa tuyển sinh.

---

## 4. CĂN CỨ VÀ NGUỒN DỮ LIỆU ĐƯA VÀO HỆ THỐNG

Tính chính xác và giá trị pháp lý của hệ thống được xây dựng trên 3 nguồn dữ liệu nền tảng:
1. **Đề Án Tuyển Sinh K71 Chính Thức:** Toàn bộ 51 trang văn bản pháp lý đã được số hóa cấu trúc, chia tách thành từng đoạn nội dung có đánh chỉ mục chương, điều, mục và số trang rõ ràng.
2. **Danh Mục 68 Chương Trình Đào Tạo Chuẩn:** Bảng dữ liệu thông số chi tiết của từng ngành, bao gồm mã tuyển sinh, chỉ tiêu của từng phương thức, tổ hợp môn, chương trình đào tạo và mức học phí.
3. **Cơ Sở Dữ Liệu Điểm Chuẩn Các Năm:** Dữ liệu điểm trúng tuyển của các năm học gần nhất theo từng phương thức xét tuyển, dùng làm căn cứ tham khảo chính xác cho thí sinh.

---

## 5. GIÁ TRỊ VÀ ĐIỂM KHÁC BIỆT CỦA HỆ THỐNG

| Tiêu Chí Đánh Giá | Chatbot Tư Vấn Thông Thường | Hệ Thống Trợ Lý Tuyển Sinh HUST 2026 |
| :--- | :--- | :--- |
| **Độ chính xác thông tin** | Thường xuyên tự suy diễn, trả lời sai lệch các quy định chi tiết. | **Chống ảo giác tuyệt đối:** Chỉ trả lời khi có căn cứ rõ ràng từ văn bản Đề án. |
| **Tính minh bạch** | Chỉ đưa ra văn bản trả lời chung chung, người dùng không thể kiểm chứng. | **Dẫn chứng minh bạch:** Luôn có nhãn số trang cụ thể kèm liên kết mở đúng trang tài liệu gốc. |
| **Xử lý số liệu phức tạp** | Dễ nhầm lẫn học phí, chỉ tiêu giữa các hệ đào tạo khác nhau. | **Đọc từ dữ liệu cấu trúc chuẩn:** Cam kết khớp số liệu 100% với phòng Đào tạo. |
| **Giải quyết câu hỏi khó** | Bế tắc, trả lời vòng vo hoặc yêu cầu thí sinh tự tìm nơi khác hỏi. | **Quy trình khép kín:** Chuyển tiếp thành Phiếu tư vấn cho Cán bộ tuyển sinh giải quyết dứt điểm. |
| **Hiệu quả vận hành** | Khó đo lường, không có công cụ cho cán bộ tiếp quản. | **Cổng làm việc chuyên biệt cho cán bộ** cùng bảng theo dõi xu hướng tuyển sinh trực quan. |

---

## 6. KẾT LUẬN

Hệ thống Trợ lý Tuyển sinh Thông minh Đại học Bách khoa Hà Nội không chỉ là một công cụ trả lời tự động, mà là một **hệ sinh thái hỗ trợ tuyển sinh toàn diện**. Hệ thống vừa giải phóng áp lực tư vấn thủ công cho đội ngũ cán bộ tuyển sinh, vừa mang lại cho thí sinh và phụ huynh một kênh tiếp cận thông tin nhanh chóng, chính xác, minh bạch và có căn cứ pháp lý cao nhất trong kỳ tuyển sinh năm 2026.
