# 1. 7-1 Pattern trong CSS

## 1. Giới thiệu về 7-1 Pattern

**7-1 Pattern** là một quy tắc tổ chức file và thư mục trong CSS (hoặc SASS/SCSS) giúp quản lý mã nguồn dễ dàng hơn, đặc biệt khi dự án có quy mô lớn.

Cấu trúc **7-1 Pattern** gồm **7 thư mục** con và **1 file chính** để tổng hợp tất cả các file SCSS thành một file duy nhất.

---

## 2. Cấu trúc thư mục của 7-1 Pattern

```scss
scss/
│   main.scss
│
├── abstracts/   # Biến, mixins, functions
│   ├── _variables.scss
│   ├── _mixins.scss
│   ├── _functions.scss
│
├── base/        # CSS cơ bản (reset, typography, elements)
│   ├── _reset.scss
│   ├── _typography.scss
│   ├── _global.scss
│
├── components/  # Thành phần nhỏ như button, card, modal
│   ├── _button.scss
│   ├── _card.scss
│   ├── _modal.scss
│
├── layout/      # Grid system, header, footer, navigation
│   ├── _grid.scss
│   ├── _header.scss
│   ├── _footer.scss
│   ├── _sidebar.scss
│
├── pages/       # CSS cho từng trang riêng biệt
│   ├── _home.scss
│   ├── _about.scss
│   ├── _contact.scss
│
├── themes/      # Chủ đề khác nhau (dark mode, light mode)
│   ├── _light.scss
│   ├── _dark.scss
│
├── vendors/     # CSS từ thư viện bên ngoài
│   ├── _bootstrap.scss
│   ├── _normalize.scss
```

---

## 3. Chi tiết từng thư mục

### 3.1. abstracts/

`Abstracts` (nhiều lập trình viên sử dụng tên "utils") là folder chứa các biến, mixins, functions giúp tái sử dụng và dễ bảo trì.

**Ví dụ:** `_variables.scss`

```scss
$primary-color: #3498db;
$secondary-color: #2ecc71;
$font-stack: "Helvetica, sans-serif";
```

Như vậy trong abstracts/ chúng ta sẽ chứa các file như:

- `_variables.scss`: chứa các biến màu sắc, font-size, font-family, ...
- `_mixins.scss`: chứa các mixins dùng để tái sử dụng code.
- `_functions.scss`: chứa các functions dùng để xử lý dữ liệu.

---

### 3.2. base/

Chứa các file SCSS cốt lõi của dự án như reset, typography, styles chung.

**Ví dụ:** `_reset.scss`

```scss
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
```

Như vậy, trong base/ chúng ta sẽ chứa các file như:

- `_reset.scss`: chứa CSS reset.
- `_typography.scss`: chứa các styles liên quan đến font-size, font-family, ...
- `_elements.scss`: chứa các styles cho các thẻ HTML.
- `_utilities.scss`: chứa các styles hữu ích như class `text-center`, `text-right`, ...
- `_animations.scss`: chứa các styles cho animation.
- `_transitions.scss`: chứa các styles cho transition.
- `_scrollbar.scss`: chứa các styles cho scrollbar (nếu có).

---

### 3.3. components/

Chứa các file liên quan đến thành phần UI nhỏ như button, card, modal.

**Ví dụ:** `_button.scss`

```scss
.button {
	background: $primary-color;
	color: white;
	padding: 10px 20px;
	border-radius: 5px;
}
```

Như vậy, trong components/ chúng ta sẽ chứa các file như:

- `_button.scss`: chứa styles cho button.
- `_card.scss`: chứa styles cho card.
- `_modal.scss`: chứa styles cho modal.
- `_form.scss`: chứa styles cho form.
- `_navbar.scss`: chứa styles cho navigation bar.
- `_slider.scss`: chứa styles cho slider.
- `_carousel.scss`: chứa styles cho carousel.
- `_pagination.scss`: chứa styles cho pagination.
- `_tabs.scss`: chứa styles cho tabs.
- `_accordion.scss`: chứa styles cho accordion.
- `_tooltip.scss`: chứa styles cho tooltip.
- `_loader.scss`: chứa styles cho loader.
- `_message.scss`: chứa styles cho message.
- `_alert.scss`: chứa styles cho alert.
- `_progress.scss`: chứa styles cho progress bar.
- `_badge.scss`: chứa styles cho badge.
- `_breadcrumb.scss`: chứa styles cho breadcrumb.
- `_dropdown.scss`: chứa styles cho dropdown.
- `_modal.scss`: chứa styles cho modal.
- `_popover.scss`: chứa styles cho popover.

Và nhiều thành phần khác nữa.

---

### 3.4. layout/

Chứa các file liên quan đến bố cục tổng thể như header, footer, navigation, grid system.

**Ví dụ:** `_header.scss`

```scss
.header {
	background: $primary-color;
	height: 60px;
	display: flex;
	align-items: center;
	padding: 0 20px;
}
```

Như vậy trong layout/ chúng ta sẽ chứa các file như:

- `_header.scss`: chứa styles cho header.
- `_footer.scss`: chứa styles cho footer.
- `_navigation.scss`: chứa styles cho navigation.
- `_grid.scss`: chứa styles cho grid system.
- `_sidebar.scss`: chứa styles cho sidebar.

---

### 3.5. pages/

Chứa styles riêng cho từng trang.

**Ví dụ:** `_home.scss`

```scss
.home {
	display: flex;
	justify-content: center;
	align-items: center;
	height: 100vh;
}
```

Như vậy, trong pages/ chúng ta sẽ chứa các file như:

- `_home.scss`: chứa styles cho trang chủ.
- `_about.scss`: chứa styles cho trang giới thiệu.
- `_contact.scss`: chứa styles cho trang liên hệ.
- `_blog.scss`: chứa styles cho trang blog.
- `_portfolio.scss`: chứa styles cho trang portfolio.
- `_services.scss`: chứa styles cho trang dịch vụ.
- `_pricing.scss`: chứa styles cho trang bảng giá.

Và nhiều trang tương ứng khác.

---

### 3.6. themes/

Chứa các file CSS cho nhiều giao diện khác nhau.

**Ví dụ:** `_dark.scss`

```scss
body {
	background: #222;
	color: #fff;
}
```

---

### 3.7. vendors/

Chứa các file CSS từ thư viện bên thứ ba như Bootstrap, Normalize.css.

**Ví dụ:** `_bootstrap.scss`

```scss
@import "bootstrap/bootstrap";
```

---

## 4. File `main.scss`

File chính dùng để import toàn bộ SCSS vào một file duy nhất.

```scss
// Importing all the scss files here

// abstracts
@import "abstracts/variables";
@import "abstracts/functions";
@import "abstracts/mixins";

// base
@import "base/reset";
@import "base/typography";
@import "base/global";

// components
@import "components/button";
@import "components/card";

// layout
@import "layout/header";
@import "layout/footer";
@import "layout/grid";
@import "layout/sidebar";

// pages
@import "pages/home";
@import "themes/dark";
@import "vendors/bootstrap";

// themes
@import "themes/dark";
```

---

## 5. Lợi ích của 7-1 Pattern

✅ Giúp tổ chức mã nguồn khoa học, dễ bảo trì.
✅ Dễ dàng mở rộng khi dự án phát triển.
✅ Giúp code rõ ràng hơn, dễ tìm kiếm và chỉnh sửa.
✅ Tránh xung đột CSS giữa các thành phần khác nhau.

---

## 6. Kết luận

**7-1 Pattern** là một chuẩn tổ chức file CSS/SASS phổ biến giúp dễ dàng quản lý code, đặc biệt cho dự án lớn. Áp dụng mô hình này giúp tăng hiệu suất và bảo trì lâu dài.

---

# 2. Thực hiện cấu trúc 7-1 Pattern trong dự án

## 1. Cài đặt các extension hỗ trợ SCSS như:

- Live Sass Compiler
- SCSS IntelliSense
- SCSS Formatter

## 2. Tạo cấu trúc thư mục

- Tạo cấu trúc thư mục như trong cấu trúc gợi ý này (file nào không cần có thể xoá đi).

## 3. Cấu hình thêm cho Live Sass Compiler

- Tạo file .vscode/settings.json
- Thêm cấu hình sau:

```json
{
	"liveSassCompile.settings.formats": [
		{
			"format": "expanded",
			"extensionName": ".css",
			"savePath": "/assets/css"
		}
	],
	"liveSassCompile.settings.generateMap": false,
	"liveSassCompile.settings.autoprefix": ["last 2 versions"]
}
```

Trong đó:

- `format`: là kiểu format của file CSS sau khi compile.
- `extensionName`: là phần mở rộng của file CSS sau khi compile.
- `savePath`: là đường dẫn lưu file CSS sau khi compile.
- `generateMap`: là cấu hình tạo source map hay không.
- `autoprefix`: là cấu hình tự động thêm các prefix CSS cho các trình duyệt.

## 4. Bắt đầu viết code

Khi code, chỉ cần ấn biểu tượng "Watch Sass" ở phía dưới bên trái để tự động compile SCSS sang CSS.

---

# Tổng kết

7-1 Pattern là một mô hình tổ chức file và thư mục trong CSS giúp quản lý mã nguồn dễ dàng hơn, đặc biệt khi dự án có quy mô lớn. Áp dụng mô hình này giúp tăng hiệu suất và bảo trì lâu dài.

Đặc biệt Devteam có nhiều thành viên cần phân chia rõ công việc tránh chồng chéo, làm giảm khả năng bị conflict code.

- Các file chỉ dùng import, không đưa trực tiếp CSS vào file SCSS có dấu `_` ở đầu, tuy nhiên khi import sẽ bỏ dấu `_` đi.

Nên tận dụng lợi thế lồng nhau của SCSS để viết code dễ dàng hơn, hiệu quả hơn. Tuy nhiên không nên lồng quá nhiều cấp độ để tránh việc khó bảo trì code.
