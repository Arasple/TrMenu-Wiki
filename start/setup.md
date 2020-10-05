---
description: 'Sau khi cài đặt plugin, các tập tin sẽ được tạo ra trong thư mục plugins'
---

# Thiết lập

## Files/Folders

{% tabs %}
{% tab title="/menus/" %}
Tệp cấu hình chính của Plugin.
{% endtab %}

{% tab title="/lang/en\_US.yml" %}
Bạn có thể chỉnh sửa hầu hết các tin nhắn của plugin trong tệp ngôn ngữ
{% endtab %}

{% tab title="/items.yml" %}
Lưu trữ cho các mục được tạo bằng lệnh `/trmenu itemRepo`
{% endtab %}
{% endtabs %}

## Setup

* Tệp `settings.yml` là tệp cấu hình chính của plugin.
* Plugin sẽ tự động phát hiện các thay đổi và tải lại tệp.

{% code title="settings.yml" %}
```yaml
#
# Cấu Hình
#
Options:
  # Có bật chế độ gỡ lỗi(debug) hay không (sẽ in thêm thông tin vào bản điều khiển(console))
  Debug: false
  # Ngôn ngữ của plugin
  # Ngôn ngữ： zh_CN, zh_TW, en_US, fr_FR, th_TH, es_MX
  Locale: en_US
  # Có ẩn Logo của plugin trong bản điều khiển(console) khi khởi động hay không
  Hide-Logo: false
  # Khi bật TrMenu sẽ lấy các dữ liệu đầu của người chơi từ Mojang của API
  # [KHUEYÉN NGHỊ] Nếu đã tắt, nó sẽ lấy chúng với https://github.com/Electroid/mojang-api
  Skull-Mojang-API: false

#
# Nhận menu từ một đường dẫn đến một thư mục hoặc trực tiếp một menu
# Hỗ trợ các tệp ItemRepo để lấy các vật phẩm làm sẵn cho menu của bạn
#
Load-Menu-Files:
  - 'plugins/CustomMenusFolder'

#
# Cấu Hình Các Hành Động
#
Actions:
  # Tùy chỉnh các từ được sử dụng để hủy trình bắt đầu vào, hỗ trợ regex
  Catcher-Cancel-Words:
    - '(?i)cancel|quit|exit|end|stop'

#
# Cấu Hình Các Vật Phẩm Menu
#
Item:
  # Màu tên mặc định của vật phẩm
  Default-Color-Name: '&7'
  # Màu lore mặc định của vật phẩm
  Default-Color-Lore: '&7'

#
# Cầu Hình Hành Động Lỗi Tắt
#
Shortcuts:
  Offhand: 'open: Example'
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  Right-Click-Player: []
  Sneaking-Right-Click-Player: []
  PlayerInventory-Border-Left: []
  PlayerInventory-Border-Right: []
  PlayerInventory-Border-Middle: []

#
# Đăng ký các lệnh vời các hành động và các argument
# Hỗ trợ tab-completition !
# (CẢNH BÁO: Yêu cầu khởi động lại máy chủ khi thêm, thay đổi hoặc xoá bỏ các lệnh)
#
RegisterCommands:
  # Tên lệnh
  openMenus:
    # Các Lệnh Bí Danh (aliases)
    aliases: []
    # Yêu cầu quyền
    permission: null
    # Các hành động thực thi mà không cần một arguments nào
    execute:
      - 'tell: &7Argument `example` Required!'
    # Arguments với cái hành động của họ
    arguments:
      example: 'open: example'

#
# Khi được bật, TrMenu sẽ bỏ qua các sự kiện huỷ bỏ được giám sát bởi một số plugin
# Nếu bạn gặp sự cố về khả năng tương thích, hãy thử chuyển đổi tùy chọn.
#
Events-Ignore-Cancelled:
  PlayerCommandPreprocessEvent: true
  InventoryOpenEvent: true
  InventoryClickEvent: true
```
{% endcode %}

