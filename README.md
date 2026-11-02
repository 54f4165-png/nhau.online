# ĐI NHẬU ONLINE 3D MULTIPLAYER — V1.4

Đã sửa trực tiếp từ ZIP V1.3 của bạn. Màn hình vào game chỉ có: **Tên nhân vật, Nam/Nữ, Trang phục, Vào chơi ngay**. Giới tính được đồng bộ qua WebSocket và thay đổi hình dáng nhân vật 3D cơ bản (tóc/váy).

## Cách triển khai
1. Triển khai `server-node` lên Render bằng Node.js (`npm install`, `npm start`).
2. Lấy URL HTTPS của Render, đổi `https://` thành `wss://`.
3. Sửa duy nhất `website-vercel/config.js`, thay `wss://THAY-BANG-SERVER-THAT.example` bằng URL thật. Người chơi sẽ không thấy ô nhập URL.
4. Đưa **nội dung bên trong** `website-vercel` lên GitHub repository MỚI (index.html phải ở thư mục gốc), deploy Vercel Framework Other, Root Directory `./`.
5. Server hiện tự chia phòng 30 người, tổng mặc định 300 kết nối/tiến trình; không phải không giới hạn thật.

**Quan trọng:** Không có URL Render thật nên chưa thể kết nối server chung ngay sau khi upload ZIP. Giao diện và đồng bộ giới tính đã cập nhật, nhưng cần cấu hình server thật.
