---
layout: post
current: post
cover: https://blog.webjeda.com/assets/thumbs/how-to-edit-add-posts-in-jekyll.jpg
navigation: True
title: Thêm và chỉnh sửa nội dung Jekyll Post trực tuyến
date: 2020-02-23 15:20:00
tags: jekyll
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

Bài viết này sẽ hỗ trợ rất nhiều cho các bạn mới làm quen với viết blog trên Github, và không quen sử dụng Markup Language. Tât nhiên, để vượt qua rào cản ngôn ngữ, bạn cần thêm công cụ. Yên tâm, bạn chẳng cần cài thêm gì trên máy tính đâu, đúng như tiêu đề là sửa trực tuyến nhé! Tất nhiên, bạn vẫn có thể sử dụng giao diện của Github để sửa nội dung file, nhưng giao diện này không thân thiện bằng công cụ mình đề xuất. Công cụ này có tên là Prose.io. Trong bài viết, mình sẽ cập nhật chi tiết về cách sử dụng Prose.io để thêm và chỉnh sửa nội dung blog.

Prose.io là một công cụ đáng tin cậy để chỉnh sửa các bài post. Giao diện, chức năng và thậm chí là hiệu ứng đều tốt. Bạn muốn up ảnh trực tiếp lên Github ử? Prose.io sẽ giúp bạn.
Khi bạn đăng nhập vào Prose, bạn sẽ thấy yêu cầu cho phép Prose chỉnh sửa repository (gọi tắt là repo) của bạn trên Github.

Bài viết được dịch từ link gốc: [Origin Post](https://blog.webjeda.com/edit-posts-jekyll/)

![prose-yeu-cau-uy-quyen](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll.png)

Sau khi bạn ủy quyền Prose, nó sẽ hiển thị tất cả các repo mà bạn sở hữu hay đóng góp trên Github.

![prose-hien-thi-danh-sach-repository](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll-2.png)

Chọn repo mà bạn dùng cho blog/website của bạn. Sau đó, di chuyển đến thư mục `_posts`, bạn sẽ thấy danh sách các post mà bạn đã đăng trên blog/website của mình.

![danh-sach-post-da-dang](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll-3.png)

Bạn có thể click **Edit** để chỉnh sửa nội dung post hoặc click **NEW FILE** để tạo bài post mới. Bạn sẽ thấy hình bên dưới khi bạn tạo post mới.

![tao-file-moi](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll-4.png)

Bạn có thể đặt tên mới và viết nội dung post bằng Markdown.

Bạn cũng sẽ thấy một số nút nhấn ở bên phải màn hình (như hình duoi71) gồm: **Edit**, **Preview**, **Meta Data** và **Save**.

![prose-menu](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll-5.png)

**Meta Data** dùng để định nghĩa _Jekyll front matter_, nơi bạn có thể thay đổi tiêu đề, ngày, tác giả, permalink,... Thuộc tính quan trọng nhất trong Meta Data là **published**. Mặc định giá trị là false, bạn cần sửa lại là true.

![gia-tri-thuoc-tinh-published](https://blog.webjeda.com/images/how-to-use-prose-io-with-jekyll-6.png)

Khi bạn tìm ra cách đồng bộ hóa các tệp và thư mục với Github từ các thư mục trên máy tính của mình, bạn sẽ nhận ra rằng Prose.io khồng còn cần thiết nữa. Nhưng đồng bộ hóa các tệp với Github có thể gây khó khăn cho nhiều người khi mới bắt đầu. Trừ khi bạn có một chút hiểu biết về **cách hoạt động của Git**, bạn không thể đồng bộ hóa thành công các tệp hoặc ít nhất là thể khắc phục sự cố đơn giản.

Đây là lý do tại sao mình giới thiệu Prose.io cho người mới bắt đầu. Nó là đơn giản, trực quan và dễ dùng.

Và nếu bạn đang sử dụng Chromebook, sẽ không có cách nào đơn giản để đồng bộ hóa các tệp Github trên máy tính. Có thể trong tương lai Github sẽ phát hành ứng dụng cho Chrome Os và Android nhưng hiện tại thì chưa có nhé!

Trong khi đi du lịch, bạn có thể chỉ đem theo điện thoại thông minh hoặc máy tính bảng bên mình. Trong những trường hợp như vậy, bạn sẽ đánh giá cao Prose.io!

_Cảm ơn vì đã đọc hết hướng dẩn của mình!_
