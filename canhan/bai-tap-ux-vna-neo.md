# Phân tích UX: Chatbot NEO (Vietnam Airlines)

## Phần 1 — Khám phá
- **Lời hứa marketing:** Trợ lý ảo AI thông minh, hỗ trợ đa tác vụ 24/7.
- **Thực tế:** Bất ngờ là NEO làm **rất tốt**! Sau khi test thực tế, bot cho thấy khả năng phân tích ngôn ngữ tự nhiên (NLP/GenAI) xuất sắc. Bot hiểu các câu hỏi dài, đa ngữ cảnh (vừa đổi vé, vừa đổi tên, vừa mua hành lý) và trả lời cực kỳ chính xác thay vì chỉ là bot bấm nút thông thường.

## Phần 2 — Phân tích 4 paths
1. **AI đúng:** Xử lý hoàn hảo các câu hỏi lắt léo. Cung cấp đầy đủ hướng dẫn trình tự các bước. (Best path). *Nhược điểm nhỏ: Câu trả lời đôi khi quá dài (Wall of text).*
2. **AI thiếu thông tin:** Khi gặp tình huống nằm ngoài kịch bản (VD: Đến sân bay trễ, tàu bay đóng cửa), bot nhận diện được là mình không biết và khuyên gọi tổng đài. (Tuy nhiên UX khúc này chưa tốt - xem Phần 3).
3. **AI sai:** Rất ít gặp do AI bám sát ngữ cảnh tốt, nếu không biết nó sẽ không nói bừa.
4. **User mất tin:** Đưa ra thông tin Hotline và Email làm phương án giải quyết cuối cùng.

*=> Đánh giá: Độ thông minh của AI rất cao, vượt kỳ vọng. Nhưng bù lại UX về mặt thiết kế giao diện (UI) chưa tối ưu cho những lúc khẩn cấp.*

## Phần 3 — Sketch "Làm tốt hơn" (Sửa Path 2: UX khi Bot bó tay)

*Tình huống: Người dùng kẹt xe, nhỡ chuyến bay nên nhắn tin trong trạng thái rất hoảng loạn. Bot trả lời không biết và ném ra 1 đoạn text dài chứa số điện thoại.*

*(Phác thảo: Vẽ khung UI Chat ra giấy theo bảng dưới đây)*

| ❌ BÊN TRÁI: Hiện tại (AS-IS) | ✅ BÊN PHẢI: Đề xuất (TO-BE) |
| :--- | :--- |
| **📱 Màn hình Chatbot**<br><br>👤 **User:**<br>╭─────────────────────────╮<br>│ Mình kẹt xe ra trễ, cửa │<br>│ máy bay đóng mất rồi,   │<br>│ hướng dẫn mình với!     │<br>╰─────────────────────────╯<br><br>🤖 **Bot:**<br>╭─────────────────────────╮<br>│ NEO hiện chưa có thông  │<br>│ tin giải quyết. Quý     │<br>│ khách vui lòng liên hệ: │<br>│ - Nội địa: 19001100     │<br>│ - Email: onlinesupport@ │<br>╰─────────────────────────╯<br><br>---<br>💥 **Điểm gãy UX:** User đang cuống cuồng mà bắt đọc nguyên 1 cục text, sau đó phải tự nhớ/copy số để mở app gọi điện. Quá mất thời gian ở tình huống khẩn. | **📱 Màn hình Chatbot**<br><br>👤 **User:**<br>╭─────────────────────────╮<br>│ Mình kẹt xe ra trễ, cửa │<br>│ máy bay đóng mất rồi,   │<br>│ hướng dẫn mình với!     │<br>╰─────────────────────────╯<br><br>🤖 **Bot:**<br>╭─────────────────────────╮<br>│ NEO chưa có nghiệp vụ   │<br>│ này. Để không trễ thêm, │<br>│ bạn hãy nối máy trực    │<br>│ tiếp với CSKH ngay nhé! │<br>╰─────────────────────────╯<br><br>👉 `[ 📞 Gọi 19001100 (Bấm gọi luôn) ]`<br>👉 `[ 🧑‍💻 Chat trực tiếp Nhân viên ]`<br><br>---<br>✨ **Thay đổi:** <br>1. Text ngắn gọn, đồng cảm hơn.<br>2. Biến số điện thoại thành **Nút bấm (Deep-link)** để user chạm 1 phát là gọi luôn, không phải copy. Thêm nút Chat nhân viên. |
