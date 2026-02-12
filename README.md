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

## 3. Lệnh dành cho Người chơi (Player Commands)
Mặc định tất cả người chơi đều có quyền sử dụng các lệnh này.

| Lệnh | Mô tả | Quyền (Permission) |
| :--- | :--- | :--- |
| `/duel <tên_người_chơi>` | Thách đấu một người chơi khác. | `solarduels.duel` |
| `/queue [join\|leave]` | Tham gia hoặc rời khỏi hàng chờ thách đấu. | `solarduels.duel` |
| `/leave` | Rời khỏi hàng chờ thách đấu. | `solarduels.duel` |
| `/spec <tên_người_chơi>` | Xem trận đấu của một người chơi. | `solarduels.spectate` |
| `/draw` | Gửi hoặc chấp nhận yêu cầu hòa trong trận đấu. | `solarduels.duel` |
| `/queue` | Mở giao diện tham gia duels. | `solarduels.duel` |

## 4. Lệnh dành cho Quản trị viên (Admin Commands)
Các lệnh này yêu cầu quyền quản trị viên.

**Lệnh chính:** `/dd` hoặc `/solarduels`
**Quyền hạn:** `solarduels.admin` (Mặc định: OP)

| Lệnh con | Mô tả |
| :--- | :--- |
| `/dd help` | Hiển thị danh sách trợ giúp lệnh admin. |
| `/dd reload` | Tải lại cấu hình plugin. |
| `/dd wand` | Lấy công cụ chọn vùng (Wand) để tạo Arena. |
| `/dd createarena <tên>` | Tạo một sàn đấu mới từ vùng đã chọn. |
| `/dd delete <tên>` | Xóa một sàn đấu. |
| `/dd setspawn <tên_arena> <1\|2>` | Đặt điểm hồi sinh cho người chơi 1 hoặc 2 trong Arena. |
| `/dd arenaregen <tên>` | Kiểm tra hoặc thử nghiệm tính năng khôi phục sàn đấu. |
| `/dd forcestop <tên_người_chơi>` | Bắt buộc dừng trận đấu của một người chơi. |

## 5. Hệ thống Quyền (Permissions)

- `solarduels.admin`: Toàn quyền quản trị (Mặc định: OP).
- `solarduels.duel`: Quyền thách đấu và tham gia hàng chờ (Mặc định: Mọi người).
- `solarduels.spectate`: Quyền xem các trận đấu (Mặc định: Mọi người).

## 6. Cấu hình
Bạn có thể tùy chỉnh thông báo, cài đặt sàn đấu và các tùy chọn khác trong file `config.yml`. Sau khi thay đổi, hãy sử dụng `/dd reload` để áp dụng.
