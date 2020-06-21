---
layout: post
current: post
cover: https://i.ibb.co/Hz9dprN/change-screen-amazingly-fast.png
navigation: True
title: "[App Inventor] Load Screen Siêu nhanh bằng Screen Ảo cho AppInventor | Thunkable | Kodular"
date: 2020-06-19 10:00:00
tags: app inventor
class: post-template
subclass: "post"
logo: assets/images/ghost.png
author: deadblox
---

Một yếu ảnh hưởng lớn tới UX chính là tốc độ. Trong bài viết này, mình sẽ giới thiệu về cách giảm thời gian chuyển giữa các màn hình khác nhau trong ứng dụng để tăng UX.

## 🔑 Giá trị bài viết này nằm ở đâu?

Bạn sẽ không thấy hiệu quả rõ rệt trong phương pháp mình giới thiệu nếu ứng dụng của bạn đơn giản, ít tài nguyên hình ảnh trong các màn hình (Screen), nhưng nếu bạn chuyển đổi qua lại giữa các màn hình chứa nhiều hình ảnh thì sẽ thất rõ điều đó - có thể nói là siêu nhanh so với cách truyền thống.

## 🔑 Tóm tắt phương pháp cũ

Đầu tiên, mình giới thiệu lại "cách tạo multiscreen - nhiều màn hình" truyền thống cho để các bạn tiện so sánh, tránh hiểu nhầm ý. Để tạo multiscreen, bạn sẽ cần nhấn nút Add Screen để thêm màn hình và chuyển màn hình bằng một sự kiện mà người dùng tương tác với App như nhấn nút "Next" mà mình thêm vào mỗi màn hình chẳng hạn.

!["Cách thêm Screen mới"](https://i.ibb.co/VS1w6wt/add-screen-gif.gif)

!["Chuyen screen bằng nút nhấn"](https://i.ibb.co/Jj6Q1n1/change-screen-by-press-button.gif)

## 🔑 Hướng dẫn phương pháp mới & so sánh

Điểm thay đổi trong phương pháp này là mình không tạo "Screen" mới. Thay vào đó, mình sử dụng linh kiện Layout như một "Screen ảo". Để làm vậy mình cần tạo nhiều Layout, mỗi Layout chứa nội dung của một Screen như trước và các Layout sẽ được điều khiển bằng lệnh để ẩn / hiện tương ứng.

!["Điều khiển hiển thị Layout"](https://i.ibb.co/PFMmcLF/control-display-layout.gif)

Vì tất cả các nội dung thực chất đang nằm trên 1 Screen và chỉ được ẩn / hiện nên không tốn thời gian tải lại tài nguyên. Bạn có thể xem hướng dẫn trong video để nắm cách làm.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PoHOX_hug5k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 🔑🔑🔑 Ưu và nhược điểm của phương pháp này

### 😁 Ưu điểm:

- Load trang siêu nhanh vì không phải tải lại tài nguyên
- Dữ liệu (biến) thuộc cùng 1 trang nên có thể dùng ngay mà không tốn thêm bước truyền dữ liệu.

### 😅 Nhược điểm:

- Quá trình thiết kế phức tạp hơn.
- Tốn thêm phần lệnh điều khiển chuyển trang (tắt /bật Layout)

😍😍😍 Nếu bạn thấy bài viết này bổ ích thì nhớ **like** để mình biết chủ đề nào các bạn cần thì sẽ làm chi tiết hơn nhé. Bạn cũng có thể đề xuất nội dung trong phần comment dưới bài viết.

😍😍😍 Đừng quên Subscribe [kênh Youtube](https://www.youtube.com/watch?fbclid=IwAR3P_N_opPMjjjyyE4j6Iwx65HAewUhYw5u4YgTcUPaz1OOE54C2-kS4PDk), có video hướng dẫn mới thì mình sẽ up trên này.
