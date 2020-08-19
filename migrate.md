---
description: Chuyển đổi các tập cấu hình từ các menu khác thành chữ của TrMenu
---

# Chuyển đổi

## Các Plugin Đã Được Hỗ Trợ

| Các Plugin | Hỗ trợ |
| :--- | :--- |
| TrMenu v1 | √ |
| DeluxeMenus | Sớm hỗ trợ |
| BossShopPro | × |
| ChestCommands | × |

## Làm Sao Để Chuyển Đổi Các Menu?

### Các Tệp Riêng Biệt

* Để chuyển đổi các tệp riêng biệt, đặt tập tin của bạn trong thư mục TrMenu và thực thi lệnh này từ bản điều khiển\(console\): `trmenu migrate <plugin> <file>`
* Các ví dụ:

  * `trmenu migrate TrMenuV1 kits.yml`

  Hoặc trong một thư mục chỉ định:

  * `trmenu migrate TrMenuV1 oldMenus/menu.yml`

### Toàn Bộ Thư Mục

* Để chuyển đổi toàn bộ thư mục menu cùng một lúc, đặt thư mục vào thư mục TrMenu của bạn và thực thi lệnh trong bản điều khiển\(console\): `trmenu migrate <plugin> <path to folder>`
* Ví dụ:
  * `trmenu migrate TrMenuV1 oldMenus`

Nếu mọi thứ trở nên tốt đẹp, bạn có thể tìm thấy tất cả menu chuyển đổi của bạn trong  `/TrMenu/migrated/`

Để tải các menu đã chuyển đổi, chỉ cần sao chép trong vào `/TrMenu/menus/` và thực thi `/trmenu reload`

