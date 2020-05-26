---
layout: post
current: post
cover: https://miro.medium.com/max/1400/0*lzRmzAy5OICef7rK.png
navigation: True
title: Những mẹo hay khi dùng Markdown Editor để viết blog
date: 2018-06-12 15:20:00
tags: jekyll
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

Có rất nhiều thứ bạn có thể làm với trình soạn thảo Markdown. Nếu bạn đã quen với việc viết bằng Markdown, thì bạn có thể sẽ thích một số mẹo nâng cao bên dưới! Bạn có thể thử các mẹo này trong lúc đọc, sẽ ghi nhớ hiệu quả hơn đấy.

## Các kiểu format

Ngoài in đậm và in nghiêng, bạn cũng có thể sử dụng một số định dạng đặc biệt khác trong Markdown, ví dụ:

+ ~~strike through~~
+ ==highlight==
+ \*escaped characters\*

## Cách viết các dòng lệnh thực hơn

Có hai loại phần tử mã có thể được chèn trong Markdown, loại đầu tiên là nội tuyến và loại còn lại là khối. Mã nội tuyến được định dạng bằng cách gói bất kỳ từ hoặc từ nào trong dấu tick ngược, `như thế này`. Các đoạn mã lớn hơn có thể được hiển thị trên nhiều dòng bằng cách sử dụng ba dấu tick ngược:

```css
.my-link {
    text-decoration: underline;
}
```

#### HTML

```html
<li class="ml-1 mr-1">
    <a target="_blank" href="#">
    <i class="fab fa-twitter"></i>
    </a>
</li>
```

#### CSS

```css
.highlight .c {
    color: #999988;
    font-style: italic; 
}
.highlight .err {
    color: #a61717;
    background-color: #e3d2d2; 
}
```

#### JS

```js
// alertbar later
$(document).scroll(function () {
    var y = $(this).scrollTop();
    if (y > 280) {
        $('.alertbar').fadeIn();
    } else {
        $('.alertbar').fadeOut();
    }
});
```

#### Python

```python
print("Hello World")
```

#### Ruby

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

#### C

```c
printf("Hello World");
```

## Reference lists

The quick brown [fox] jumped over the lazy [dog].
```
The quick brown [fox] jumped over the lazy [dog].

[fox]: https://en.wikipedia.org/wiki/Fox
[dog]: https://en.wikipedia.org/wiki/Dog
```

Một cách khác để chèn liên kết trong markdown là sử dụng danh sách tham chiếu. Bạn có thể muốn sử dụng kiểu liên kết này để trích dẫn tài liệu tham khảo theo kiểu Wikipedia. Tất cả các liên kết được liệt kê ở cuối tài liệu, vì vậy bạn có thể duy trì sự tách biệt hoàn toàn giữa nội dung với nguồn hoặc tài liệu tham khảo.

## Full HTML

Có lẽ phần hay nhất của Markdown là bạn không bao giờ bị giới hạn chỉ với Markdown. Bạn có thể viết HTML trực tiếp trong trình soạn thảo Markdown và nó sẽ hoạt động bình thường. Không giới hạn nào cả! Mình lấy mã nhúng YouTube tiêu chuẩn làm ví dụ:

<p><iframe style="width:100%;" height="315" src="https://www.youtube.com/embed/Cniqsc9QfDo?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe></p>

[fox]: https://en.wikipedia.org/wiki/Fox
[dog]: https://en.wikipedia.org/wiki/Dog