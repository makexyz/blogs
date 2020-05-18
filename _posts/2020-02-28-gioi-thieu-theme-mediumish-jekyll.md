---
layout: post
current: post
cover: https://bootstrapstarter.com/assets/img/themes/mediumish-jekyll.jpg
navigation: True
title: Giới thiệu theme Jekyll Mediumish siêu đẹp
date: 2020-02-28 15:00:00
tags: jekyll
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

## Tính năng

1. Được xây dựng cho Jekyll
2. Tương thích với Github pages
3. Bài viết nổi bật (Featured Posts)
4. Đánh số phân trang (Index Pagination)
5. Tối ưu hóa cho công cụ tìm kiếm (SEO)
6. Feed
7. Sơ đồ trang (Sitemap)
8. Chia sẻ bài viết (Post Share)
9. Phân loại bài viết (Post Categories)
10. Bài viết kế tiếp / trước đó (Prev/Next Link)
11. Category Archives (Compatible with Github pages)
12. Jumbotron Categories
13. Đánh giá trên bài viết (Post Reviews with Stars)
14. Bôi mờ đoạn văn bản (Blurred Spoilers)
15. Danh sách nội dung tự động (Table of Content)
16. Lazy Load Images
17. Tích hợp:
    * Disqus Comments => Dành cho đánh giá
    * Google Analaytics => Dành cho thống kê tự động số truy cập vào trang
    * Mailchimp Integration => Dành cho đăng ký nhận tin
    * Adsense => Dành để chèn quảng cáo từ Google
18. Các tính năng thiết kế nổi bật:
    * Bootstrap v4.x
    * Font Awesome
    * Masonry
19. Các dạng Layout:
    * Default
    * Post
    * Page
    * Archive
    * Categories (100% tương thích với Github pages)

![Mediumish Theme Demo](https://bootstrapstarter.com/assets/img/themes/mediumish-jekyll.jpg)

## Jekyll là gì

Nếu bạn chưa từng nghe về Jekyll thì nó là một dạng phần mềm cung cấp giải pháp tạo ra trang web tĩnh từ những thông tin có sẵn và layout có sẵn. Nói cách khác, nó giúp biến file text chứa nội dung post mà bạn viết thành một post hoặc một web tĩnh. Bạn sẽ không cần database, không còn chuyện load trang chậm hay rủi ro bị hack... Do đó, bạn sẽ có nhiều thời gian dành cho nội dung viết hơn. Và thú vị nhất vẫn là, với Jekyll bạn có thể tạo một trang web miễn phí với tài khoản Github. Bạn nên dành thời gian đọc sơ tài liệu về Jekyll để nắm thêm thông tin nếu mới tìm hiểu. Nếu bạn đã có kiến thức cơ bản về Jekyll rồi thì mình chuyển sang phần cài đặt theme Mediumish cho Jekyll như bên dưới.


## Cách sử dụng theme “Mediumish”

### Tải theme Mediumish
Tải về theme Mediumish bằng cách vào command prompt, lần lượt gõ lệnh bên dưới
Lưu ý: Bạn cần cài Ruby trước để  sử dụng lệnh `bundle`.

```
git clone https://github.com/wowthemesnet/mediumish-theme-jekyll.git
cd mediumish-theme-jekyll
bundle
```

### Chỉnh file _config.yml

Nếu trang web của bạn được lưu trong thư mục gốc luôn thì chỉnh `baseurl: ''`. Bạn cũng cần chỉnh mã Google Analytics, disqus username, authors, Mailchimp list nếu có sử dụng


Sau khi chỉnh xong, bạn có thể khởi tạo Server trên máy tính để xem trang với lệnh sau:

```
bundle exec jekyll serve --watch
```

Bạn có thể tạo bài viết mới bằng cách tạo file **.md** trong thư mục **_posts**. Mediumish cũng đã có sẵn nhiều ví dụ cho bạn tham khảo.

**YAML front matter**

* Bật tính năng bài viết nổi bật - `featured:true`
* Loại các bài viết nổi bật khỏi “All stories” để tránh lặp lại - `hidden:true`
* Ảnh bài viết - `image: assets/images/mypic.jpg`
* Ảnh bài viết với link bên ngoài - `image: "https://externalwebsite.com/image4.jpg"`
* Bật tính năng comment - `comments:true`
* Mô tả nội dung trường meta (không bắt buộc) - `description: "this is my meta description"`

### Ví dụ YAML Post

```
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/5.jpg
description: "Something about this post here"
---
```

### Ví dụ YAML Page

```
---
layout: page
title: Mediumish Template for Jekyll
comments: true
---
```

### Ví dụ Đánh giá

```
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/5.jpg
description: "Something about this post here"
rating: 4.5
---
```

### Quảng cáo Adsense

Bật tính năng quảng cáo bằng cách điều chỉnh file _config.yml.

Adsense (thay giá trị thành "enabled" để kích hoạt). Bạn cũng cần cập nhật giá trị `adsense-data-ad-client` và `adsense-data-ad-slot` cho tương thích với khai báo quảng cáo của bạn trên tài khoản Google Adsense.

```
adsense: "disabled"
adsense-data-ad-client: "ca-pub-3412143450191416"
adsense-data-ad-slot: "1363087678"
```

### Lazy Load Images

Bật tính năng này bằng cách điều chỉnh file _config.yml.

Lazy Images ("enabled" hoặc "disabled")

```
lazyimages: "enabled"
```

### Table of Contents

Add toc:true on your post YAML.

```
---
layout: post
title:  "Education must also train one for quick, resolute and effective thinking."
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/3.jpg
beforetoc: "Markdown editor is a very powerful thing. In this article I'm going to show you what you can actually do with it, some tricks and tips while editing your post."
toc: true
---
```

beforetoc thêm một đoạn văn bản trước khi hiển thị TOC.
