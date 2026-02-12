# Hướng dẫn sử dụng SolarDuels

## 1. Cài đặt Đấu trường (Arena/Map)
Để tạo một map mới, bạn cần thực hiện các bước sau:

1.  **Lấy công cụ chọn vùng:** Sử dụng lệnh `/dd wand` để lấy Rìu Vàng (Arena Selection Wand).
2.  **Chọn vùng đấu trường:**
    *   Chuột trái vào block thứ nhất để chọn Corner 1.
    *   Chuột phải vào block thứ hai để chọn Corner 2.
3.  **Tạo Map:** Sử dụng lệnh `/dd create <tên_map>`.
4.  **Đặt vị trí Spawn:**
    *   Đứng tại vị trí người chơi 1 sẽ xuất hiện và gõ: `/dd setspawn1 <tên_map>`.
    *   Đứng tại vị trí người chơi 2 sẽ xuất hiện và gõ: `/dd setspawn2 <tên_map>`.
5.  **Hoàn tất:** Map sẽ tự động kích hoạt nếu đã đủ thông tin.

## 2. PlaceholderAPI (PAPI)
Plugin hỗ trợ các Placeholder sau để hiển thị thông số người chơi (yêu cầu cài đặt PlaceholderAPI):

*   `%solarduels_wins%`: Số trận thắng.
*   `%solarduels_losses%`: Số trận thua.
*   `%solarduels_winrate%`: Tỉ lệ thắng (%).
*   `%solarduels_kills%`: Số mạng hạ gục trong duel.
*   `%solarduels_deaths%`: Số lần chết trong duel.
*   `%solarduels_streak%`: Chuỗi thắng hiện tại.
*   `%solarduels_status%`: Trạng thái người chơi (Trong trận, Đang chờ, v.v.).

## 3. Các lệnh cơ bản
*   `/duel <tên_người_chơi>`: Gửi lời mời thách đấu.
*   `/duel accept <tên_người_chơi>`: Chấp nhận lời mời.
*   `/duel decline <tên_người_chơi>`: Từ chối lời mời.
*   `/leave`: Rời khỏi trận đấu hiện tại.
*   `/spectate <tên_người_chơi>`: Xem trực tiếp trận đấu.

## 4. Cấu hình Quan trọng (config.yml)
*   `KEEP-ITEMS`: Nếu là `true`, người chơi không mất đồ khi chết trong duel.
*   `ALWAYS_IN_DUEL_WORLD`: Nếu là `true`, khán giả sẽ ở lại thế giới duel sau khi trận đấu kết thúc thay vì quay về vị trí cũ.
