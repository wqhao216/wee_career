# wee_career

Portfolio của Hoàng Quân Hạo, đăng tại https://wqhao216.github.io/wee_career/

HTML, CSS và JavaScript thuần. Không framework, không bước build. Mở `index.html` là xem được.

## Sửa chữ

Toàn bộ chữ nằm trong `i18n/en.js` (tiếng Anh, mặc định) và `i18n/vi.js` (tiếng Việt). Hai file có cùng bộ khóa. Sửa giá trị trong cả hai file, không sửa chữ trong HTML.

Chỗ còn thiếu thông tin được đánh dấu `[TODO: ...]`. Tìm nhanh bằng cách tìm chữ `TODO` trong hai file trên.

## Thêm hoặc thay ảnh

Ảnh nằm trong `assets/img/`. Thay ảnh cũ thì chép file mới đè lên, giữ đúng tên. Thêm ảnh mới thì viết thẻ `<img>` giống các ảnh đã có, nhớ ghi `width`, `height` và `loading="lazy"`, và thêm mô tả ảnh (alt) vào cả `i18n/en.js` lẫn `i18n/vi.js`.

Ảnh màn hình máy tính nên rộng khoảng 1600 px, ảnh điện thoại khoảng 720 px, nén JPG chất lượng 75 đến 80%.

CV nằm ở `assets/cv/Hoang-Quan-Hao-CV.pdf`. Cập nhật CV thì chép file mới đè lên, giữ đúng tên.

## Cấu trúc

```
index.html              trang chủ
work/the-hook/          case study The Hook
work/bloommate/         case study BloomMate
work/lume/              case study Lumé
about/                  giới thiệu
404.html                trang lỗi (dùng <base href="/wee_career/">)
i18n/                   chữ hai ngôn ngữ
assets/css, js, fonts, img, cv
```

Font Be Vietnam Pro, giấy phép SIL Open Font License (`assets/fonts/OFL.txt`).

Nếu đổi tên repo, sửa đường dẫn `/wee_career/` trong thẻ `canonical`, `og:url`, `og:image` của các trang và trong `<base>` của `404.html`.
