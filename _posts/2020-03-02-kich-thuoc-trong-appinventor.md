---
layout: post
current: post
cover: https://i.ibb.co/n6t2Nhv/px-vs-dp.jpg
navigation: True
title: Lỗi đơn vị kích thước tuyệt đối trong App Inventor
date: 2020-03-02 10:18:00
tags: app inventor
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

Bài viết này chỉ ra 1 lỗi sai nghiêm trọng về đơn vị đo sẽ khiến các bạn không kiểu gì hình dung được tại sao mình thiết kế một đằng nhưng App Inventor lại hiển thị một nẻo trong Responsive Mode.

![Screen Sizing in App Inventor](https://i.ibb.co/vLZbkg3/Screen-Sizing.png)

## VẤN ĐỀ

Trong phần điều chỉnh kích thước của các Component, App Inventor cho tùy chọn kích thước tuyệt đối (pixel) và kích thước tương đối so với màn hình (percent). Làm một ví dụ đơn giản, mình muốn thiết kế cái nút nhấn dài đúng 50% chiều rộng màn hình của mình nhưng khai báo ở chế độ tuyệt đối (px). Màn hình điện thoại của mình có độ phân giải HD+ (1080x2232 px).

> Nếu bạn nghĩ, ở chế độ Responsive của App Inventor và điền vào ô kích thước Width = 540px (thuộc tính của nút nhấn - giá trị tuyệt đối) sẽ khiến cái nút nhấn dài 1 nửa so với chiều dài của màn hình thì bạn lầm to rồi. Thực tế, cái nút nhấn sẽ dài còn hơn cả chiều rộng màn hình luôn!

![Pixels vs Percent in Measurement](https://i.ibb.co/ftryj12/Pixels-vs-percent.png)

## NGUYÊN NHÂN

Lý do là vì **đơn vị viết tắt mà App Inventor đang sử dụng là không đúng.** Nó không phải là Pixcel (viết tắt px) mà phải là Device-independent Pixel (viết tắt dp). Dp là một đơn vị đo chiều dài vật lý cũng giống như inch, cm, mm… mà Google thường áp dụng để đo kích thước màn hình của thiết bị. (Bên iOS dùng pt hay point có khái niệm tương tự với dp).

Tưởng tượng thế này, bạn có 2 cái laptop 14 inch, chiều dài và chiều rộng của 2 màn hình bằng nhau (dài x rộng: XX x YY cm) nhưng cái thứ nhất có độ phân giải (1366x768 px), cái thứ hai có độ phân giải (1920x1080 px) thì rõ ràng, nếu hiển thị nội dung có độ phân giải >= 1920x1080 px thì 100% cái thứ 2 sẽ sắc nét hơn. Nhưng, cả 2 cái đều sẽ có kích thước ứng với đơn vị dp như nhau vì cùng kích thước vật lý thực tế cm.

Trên các thiết bị có độ phân giải khác nhau nhưng kích thước thực tế bằng nhau thì dp bằng nhau. 1 dp có thể là 1 hay nhiều px. Điều này giúp tạo nên tính đồng bộ trong nội dung hiển thị trên các thiết bị có độ phân giải khác nhau.

![Device-indendent Pixel and Screen Density](https://i.ibb.co/tZ6fG3x/pixel-density.png)

Và, App Inventor sử dụng đơn vị dp chứ không phải px như hiển thị ra màn hình nhé! Điện thoại của mình có độ phân giải thực tế là: 1080x2232 (px) nhưng với kích thước màn hình thực tế, quy đổi ra dp thì chỉ là: 360x696(dp). Tham số đo dp này hoàn toàn có thể lấy ra bằng các khối lệnh trong phần lập trình (Block) của component Screen1 (Screen1.Width, Screen1.Height)

![Fixed Mode vs Responsive Mode in App Inventor](https://i.ibb.co/0yNTrMy/fixed-Mode-vs-responsive-Mode.png)

## TẠI SAO CẦN QUAN TÂM

Đúng là nếu để đơn vị Percent (%), bạn sẽ có thể kiểm soát được kích thước Component hiển thị đúng tỷ lệ mình muốn trên các màn hình có độ phân giải khác nhau. Nhưng, bạn có thể kiểm soát được kích thước Font chữ không?

Cái nút trên ứng dụng của bạn được khai báo Width = 50% sẽ luôn hiển thị chính xác là 50% chiều rộng màn hình dù trên điện thoại hay tablet. Tuy nhiên, cái nút với Font Size = 16 hiển thị rất đẹp trên điện thoại thì lại vô cùng lởm trên tablet khi chữ quá nhỏ so với viền nút! Font Size được tính toán dựa trên Dp nên sẽ hiển thị tương đối như nhau trên các thiết bị có độ phân giải khác nhau.

Hiểu được sự khác biệt giữa px và dp sẽ là cơ sở giúp bạn phân loại được đâu là điện thoại, đâu là tablet để thiết kế giao diện cho phù hợp. Điện thoại của mình có độ phân giải (px) rất cao, cao hơn nhiều so với các tablet tầm thấp và cận trung nhưng nó vẫn là điện thoại vì dp của nó chưa đủ để là tablet!

## TÀI LIỆU THAM KHẢO

Link hay mà các bạn có thể tham khảo trong thiết kế Responsive với App Inventor

1. [Kích thước thiết bị](https://material.io/resources/devices/)
2. [Đo độ phân giải màn hình của bạn](https://www.mydevice.io/#compare-devices)
3. [AppyBuilder TIPS: Responsive App Design (Best Practices, Concepts) - YouTube](https://www.youtube.com/watch?v=DYuzZWudt0w)
4. [Responsive Design in App Inventor](http://ai2.appinventor.mit.edu/…/other/responsiveDesign.html)
