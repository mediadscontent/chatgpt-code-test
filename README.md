# Sparkle Salon — nhánh sparkle-salon

Game makeover bản thử nghiệm. Web preview chơi được trên trình duyệt, tối ưu iPhone (ảnh progression 8 khung dùng một WebP atlas).

## Xem và chơi
- Vào thư mục `web` và mở `index.html` qua HTTP server.
- `python3 -m http.server 8000` tại thư mục repo, sau đó mở `http://localhost:8000/web/`.
- Để mở trên iPhone từ Internet, triển khai thư mục `web/` lên một hosting HTTPS; branch GitHub không tự tạo website công khai.

## Gameplay
- 7 bước: gỡ tóc, làm sạch, chăm sóc mụn, chân mày, mắt, làm tóc, makeup.
- Sử dụng vuốt theo hướng/chà/giữ, chuyển đổi ảnh nhân vật theo tiến độ, Before/After.
- 30 cấp màn có lặp lại nhiệm vụ; chỉ là bản prototype, chưa xác nhận đạt mục tiêu 40 phút/IPU.
- Các mục tóc rối đặt trên tóc lộ ra ngoài khăn, không chải lên khăn quấn.

## Native
Bộ HS Native SDK 1.1.3 và bản game Native đã được cung cấp riêng trong gói ZIP của cuộc hội thoại. Chưa xác minh cloud/ads production vì thiếu Game ID, App ID và Ad IDs.
