# LexiVN — Website tra cứu từ điển tiếng Anh

## Công nghệ
- HTML5, CSS3, JavaScript thuần.
- Dictionary API: https://dictionaryapi.dev/
- Translation fallback: MyMemory Translation API.
- AI translation tùy chọn: Gemini API (người dùng tự nhập API key trong trang Tài khoản).
- Text-to-Speech: Web Speech API `speechSynthesis`.
- Speech-to-Text: Web Speech API `SpeechRecognition`/`webkitSpeechRecognition`.
- Login/Register, yêu thích, lịch sử, giao diện sáng/tối: `localStorage`.

## Chạy
Mở `index.html` bằng trình duyệt. Nếu trình duyệt chặn một số request CORS khi mở bằng file://, chạy một static server đơn giản, ví dụ VS Code Live Server.

## Các route
- `#home`: Trang chủ
- `#dictionary/word`: Tra từ
- `#favorites`: Từ yêu thích
- `#history`: Lịch sử
- `#quiz`: Luyện tập
- `#login`, `#register`: Đăng nhập/đăng ký
- `#profile`: Tài khoản + cấu hình Gemini

## Lưu ý học thuật
Đăng nhập/localStorage ở đây là mô phỏng phía trình duyệt, không phải cơ chế xác thực an toàn cho hệ thống thực tế. API key Gemini nếu nhập ở trình duyệt cũng có thể bị lộ; khi triển khai thực tế nên đưa lời gọi mô hình qua backend/proxy.
