---
layout: post
current: post
cover: https://i.ibb.co/ThB29vx/arduino-vs-raspberry.png
navigation: True
title: Board nào tốt hơn - Raspberry hay Arduino
date: 2020-05-29 10:00:00
tags: arduino
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

> Bạn đang phân vân không biết chọn board mạch điều khiển nào cho dự án tự động của bạn thì đây là bài viết bạn nên đọc.

Có rất nhiều mạch điện tử điều khiển mà bạn có thể dùng trong những dự án tự động / thông minh. Hai đại diện tiêu biểu được nhiều người biết đến là board Arduino và board Raspberry. Vậy mình nên chọn board mạch nào cho dự án của mình thì hợp lý nhất vì nhìn sơ bên ngoài thì 2 board mạch này có kích thước khá tương đồng, chúng có các cổng kết nối và có chip điều khiển lập trình được. Sau bài viết này bạn sẽ nắm được sự khác biệt cơ bản giữa Arduino và Raspberry Pi và từ đó chọn đúng board điều khiển cho dự án của mình.

## Arduino (Uno) xây dựng trên một Vi Điều Khiển

Mình sẽ bắt đầu với board Arduino Uno, đây là một đại diện tiêu biểu của dòng board Arduino. Arduino Uno được xây dựng dựa trên vi điều khiển ATmega 328P. Trong con vi điều khiển này là 2Kb RAM, 32Kb bộ nhớ FLASH, một vài bộ định thời (giống như kiểu đồng hồ báo thức) và phần cứng phục vụ giao tiếp giữa nó và các thiết bị bên ngoài khác như Serial, I2C, SPI. Trên board mạch, bên ngoài con chip là các bộ chia áp, linh kiện điện tử như điện trở, tụ điện,... và các cổng giao tiếp. Chương trình mà bạn viết trên Arduino IDE sẽ được biên dịch và lưu trên bộ nhớ của vi điều khiển ATmega 328P. Arduino Uno (hay ATmega 328P) không có firmware hay hệ điều hành nào gắn với nó cả, chỉ có chương trình bạn nạp.

## Raspberry Pi xây dựng trên một Vi Xử Lý

Trong khi đó, Raspberry Pi là một kiểu máy tính thu nhỏ (Single Board Computer) có đủ CPU (chip vi xử lý), ~2Gb bộ nhớ RAM, cổng kết nối HDMI, Audio, USB Host, Ethernet, thẻ SD như máy tính bình thường. Raspberry Pi được xây dựng dựa trên vi xử lý ARM đa lõi với tốc độ xử lý lên đến 1.4GHz và hơn thế trong khí 328P chỉ có tốc độ xử lý chỉ đến 20MHz. Đến đây thì chắc các bạn cũng thấy sự khác biệt lớn. Raspberry Pi cũng có các chân kết nối thiết bị điện tử bên ngoài như Arduino. Tuy nhiên, các chân này do hệ điều hành chạy trên Raspberry điều khiển trực tiếp, chương trình của bạn trên Raspberry chỉ nói cho hệ điều hành thông tin để điều khiển chứ không trực tiếp điều khiển như trên Arduino.

<iframe width="1280" height="720" src="https://www.youtube.com/embed/7vhvnaWUZjE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Vi điều khiển và vi xử lý thì khác gì nhau

Vi xử lý và vi điều khiển đều có khả năng tính toán và xử lý tuy nhiên vi xử lý có tốc độ xử lý cao hơn vi điều khiển rất nhiều (GHz vs MHz). Nói cách khác thì Raspberry Pi có não to hơn Arduino Uno, tính toán và xử lý nhanh hơn rất nhiều (>40 lần). Không chỉ nhanh hơn, Raspberry còn có bộ nhớ RAM lớn hơn Arduino rất nhiều (2Gb hay 2048Mb vs 2Mb). Với RAM nhiều hơn, Raspberry có thể xử lý các file dung lượng lớn vì có đủ chỗ chứa tạm. => _**Raspberry WIN**_
Vi xử lý và vi điều khiển đều có các chân kết nối ngoại vi (IO pin) nhưng điện áp trên IO pin của vi xử lý thường ở mức 3.3V (điện áp thấp) khiến nó khó điều khiển trực tiếp các thiết bị khác so với vi điều khiển, có mức điện áp IO pin là 5V. Vẫn chưa hết nhé, dòng điện tối đa trên các IO pin cũng chênh lệnh lớn: Ở Arduino là max 40mA, ở Raspberry chỉ khoảng 5mA. => _**Arduino WIN**_
Xét về giá thì một board Arduino Uno chỉ khoảng 120.000VND rẻ hơn nhiều một board Raspberry Pi - giá khoảng 650.000VND => _**Arduino WIN**_

## Khi nào thì dùng board gì ^^!

Câu trả lời dựa trên tính chất đặc thù của dự án, chi phí cho dự án, tính phức tạp và việc mở rộng các chức năng của dự án.

Mình lấy ví dụ như sau: Nếu bạn chỉ cần điều khiển vài thiết bị điện tử một cách tự động thì dùng Arduino Uno hoặc các dòng tương tự là đủ và thậm chí là dư sức chơi rồi. Dự án của bạn lớn dần lên khi bạn muốn điều khiển các thiết bị điện tử trước đó qua mạng Wifi, bạn cũng chỉ cần lắp thêm module giao tiếp Wifi chứ chưa cần đổi board điều khiển Arduino. Dự án của bạn lớn thếm nữa, đòi hỏi phải lưu lại dữ liệu thu về từ 1 trong các thiết bị này để thống kê, bạn cũng vẫn không cần đổi board điều khiển mà chỉ cần lắp thêm module thẻ nhớ để lưu dữ liệu lên thẻ. Nhưng rồi bạn muốn làm 1 server điều khiển, có thể kết nối được từ điện thoại di động và bạn có thể điều khiển / đọc dữ liệu các thiết bị kia qua giao diện Web được server cung cấp thì chắc là bạn cần mua thêm board Raspberry để sử dụng cùng với Arduino rồi đó. Hoặc bạn cần kích hoạt đèn trong nhà chẳng hạn qua hình ảnh thu về từ camera (khi có người trong phòng) thì chắc 100% là bạn cần Raspberry Pi vì Arduino Uno không đủ bộ nhớ RAM để hỗ trợ xử lý hình ảnh.

Tóm lại, khi bạn chỉ làm dự án thuần về điều khiển thông thường, không dính đến xử lý ảnh, trí thông minh nhân tạo, hiển thị ảnh màu tốc độ cao... thì Arduino là đủ rồi. Và thường thì Raspberry chỉ xuất hiện khi bạn phát hiện ra trong dự án của mình có phần nào đó cần khả năng xử lý vượt qua khả năng xử lý của Arduino hay yêu cầu RAM lớn thôi.

Mình hy vọng sau bài viết này thì bạn cũng chọn được board mạch nào dùng cho dự án của mình nhé!

Credit: Bài viết có sử dụng thông tin trong clip [Arduino vs. Raspberry Pi - Which is best? | AddOhms #7](https://www.youtube.com/watch?v=7vhvnaWUZjE&fbclid=IwAR1GS1iK53Q284I0U-6qoDxxey8u_h2Z0xoGs0nZrkeTXXDy46S28VdL550)