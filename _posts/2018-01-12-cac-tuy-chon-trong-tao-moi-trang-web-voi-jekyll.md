---
layout: post
current: post
cover: https://jekyllrb.com/img/jekyll-og.png
navigation: True
title: Các tùy chọn trong việc tạo trang web mới với Jekyll
date: 2018-01-12 10:00:00
tags: jekyll
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

`jekyll new <PATH>` giúp cài đặt một trang web Jekyll mới tại đường dẫn được chỉ định (liên quan đến thư mục hiện tại). Trong trường hợp này, Jekyll sẽ được cài đặt trong một thư mục có tên `myblog`. Dưới đây là một số chi tiết bổ sung:

- Để cài đặt trang Jekyll vào thư mục bạn hiện đang ở, hãy chạy `jekyll new`. Nếu thư mục hiện tại không trống, bạn có thể  thêm tùy chọn --force
- `jekyll new` tự động khởi động `bundle install` để cài đặt các phụ thuộc cần thiết. (Nếu bạn không muốn Bundler cài đặt gem, hãy sử dụng `jekyll new myblog --skip-bundle`.
- Theo mặc định, trang web Jekyll được cài đặt bởi `jekyll new` sử dụng một chủ đề có tên là Minima. Với các chủ đề dựa trên gem như Minima, một số thư mục và tệp được lưu trữ trong theme bị ẩn khỏi chế độ xem tức thời của bạn.
- Bạn nên thiết lập Jekyll với chủ đề dựa trên đá quý nhưng nếu bạn muốn bắt đầu với một bản trống, hãy sử dụng `jekyll new myblog --blank`
- Để tìm hiểu về các tham số khác, bạn có thể  nhập `jekyll new --help`.
