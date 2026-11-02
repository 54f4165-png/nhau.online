# ĐI NHẬU ONLINE 3D — SERVER CHUNG V1.3

## Người chơi
Chỉ nhập tên, chọn áo, bấm VÀO QUÁN NGAY. Không nhập địa chỉ server, không nhập mã phòng.

## Chủ game — cần thiết lập một lần
1. Triển khai thư mục `server-node` lên Render / Railway / VPS chạy Node.js 20+ (lệnh `npm install` và `npm start`).
2. Lấy địa chỉ HTTPS của server, đổi `https://` thành `wss://`.
3. Trong `website-vercel/config.js`, thay `wss://THAY-BANG-SERVER-THAT.example` bằng URL WSS thực tế.
4. Đưa **chỉ nội dung** thư mục `website-vercel` vào repository GitHub riêng; deploy Vercel Framework Other, Root Directory `./`.
5. Người chơi truy cập URL Vercel, tự vào phòng còn chỗ. Khi QUAN-1 đủ 30 người sẽ tự chuyển QUAN-2, QUAN-3...

## Giới hạn thực tế
Không có giới hạn cố định 30 người cho toàn server. Mỗi phòng 3D vẫn tối đa 30 người để bảo đảm hiển thị/hiệu năng. Mặc định MAX_TOTAL=300 trên một tiến trình, chỉnh bằng biến môi trường và kiểm thử tải trước khi tăng. Người ở các phòng khác nhau không nhìn thấy nhau. Server hiện lưu trạng thái trong RAM; khởi động lại sẽ ngắt phiên chơi. Không hỗ trợ cân bằng tải nhiều instance nếu chưa có hệ thống phân phối phòng chung.

## Chạy thử trên máy
`cd server-node && npm install && npm start`; đặt URL `ws://localhost:8080` trong config.js khi thử local. Khi deploy website HTTPS phải dùng WSS.
