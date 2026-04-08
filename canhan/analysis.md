# Ghi chú phân tích Chatbot NEO (Vietnam Airlines)

## 1. Phân tích 4 Paths

Dựa trên kết quả "stress test" bằng các câu hỏi nhiều tình huống ép góc, dưới đây là phân tích 4 paths của sản phẩm:

- **Path 1: Khi AI đúng (Xử lý tốt nhất)**
  - NEO xử lý hoàn hảo các câu lệnh lắt léo (hỏi cùng lúc chuyện đổi vé và mua hành lý bổ sung). Nó tách đúng các ý và cung cấp đầy đủ trình tự giải quyết.
  - *Ghi chú nhỏ:* Tuy giải quyết tốt nghiệp vụ, nhưng UI hiển thị văn bản trả lời đôi khi quá dài (Wall of text).

- **Path 2: Khi AI thiếu thông tin / Không có nghiệp vụ (Điểm gãy UX)**
  - Khi người dùng gặp sự cố khẩn (vd: trễ sân bay, đóng cửa tàu bay), bot nhận diện được là mình không có hướng dẫn nên chuyển luồng sang tổng đài. 
  - *Ghi chú điểm gãy:* Lúc người dùng đang khẩn cấp, bot lại cung cấp thông tin dưới dạng một đoạn văn bản (liệt kê sđt, email). Bắt người dùng tự nhớ hoặc copy số điện thoại thay vì có Nút bấm (Button) gọi điện ngay trên mặt chat.

- **Path 3: Khi AI sai**
  - Hầu như không xuất hiện. Ứng dụng AI khá thông minh (khả năng suy luận tốt) và đưa ra phán đoán cực chuẩn, nếu nằm ngoài giới hạn nó sẽ nhảy ngay về Path 2 để nhờ cứu viện chứ không "bịa" ra thông tin (no hallucination).

- **Path 4: Khi user cần fallback**
  - Có đầy đủ các lối thoát hiểm: Hotline nội địa/quốc tế, Email, và Nút chọn gặp nhân viên thực. Trợ giúp user thoát khỏi tình trạng mắc kẹt.

---

## 2. Nhận xét Gap giữa Marketing và Thực tế

- **Lời hứa Marketing:** Trợ lý ảo thông minh, người bạn đồng hành số.
- **Dữ liệu thực tế:** AI não bộ (Backend GenAI) xử lý ngôn ngữ siêu việt, bắt kịp mọi ngữ cảnh nhiễu, xứng danh "thông minh". Hoàn toàn đáp ứng được lời hứa marketing về mặt năng lực xử lý vấn đề.
- **Gap (Độ vênh):** Có sự chênh lệch lớn giữa "não AI xịn" và "giao diện UI/UX chưa tinh tế". Trong khi AI trả lời rất sắc bén, form UI lại thiên về việc phô diễn tin nhắn chữ vách tường dài dòng. Đặc biệt lúc người dùng hoảng sợ/gấp gáp nhất, UX thiếu những Micro-actions thiết yếu (như Nút call-to-action tích hợp nhấn-để-gọi) làm tính "trợ lý chăm sóc" bị giảm đi đáng kể. Lẽ ra một AI thông minh phải đi kèm với một UI thấu cảm.
