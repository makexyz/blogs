---
layout: post
current: post
cover: https://i.ibb.co/1nS2pXL/arduino-library-conflict.jpg
navigation: True
title: Xung giữa các thư viện Arduino
date: 2020-05-28 10:00:00
tags: arduino
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

> Khi bạn đặt tất cả các đoạn code lại với nhau theo logic nhưng chương trình Arduino không chạy .. vì xung đột thư viện thì bài viết này bạn nên đọc!

## Không sử dụng thư viện thì khỏi xung đột ?

Đúng là không xài thư viện thì sẽ né được nguy cơ này khá cao! Nhưng ai đã và đang tìm hiểu Arduino đều ý thức được rằng thứ đáng giá nhất ở Arduino chính là bộ thư viện giao tiếp phần cứng đồ sộ của nó, được xây dựng và đóng góp cộng đồng Arduino trên toàn thế giới. Mình thề rằng trong rất nhiều trường hợp những thư viện này rút gọn thời gian tìm hiểu và viết code cho ứng dụng điều khiển tự động từ cả tháng xuống chỉ còn một vài ngày. Ah, cả tháng đó là đối với dân bán chuyên hoặc chuyên lập trình thôi, còn dân không chuyên lập trình thì quên luôn đi :)

## Lý do có sự xung đột giữa các thư viện

Nói nhảm xíu, các bạn có biết cuộc chiến Android vs iOS không? Android nổi tiếng ở mã nguồn mở, tính tùy biến cao nhưng tới giờ cũng chưa nuốt nổi iOS. Lý do sao vậy? iOS có tính ổn định và tính hệ thống tốt hơn Android. Nó được phát triển bởi 1 nhà sản xuất duy nhất nên iOS trên Iphone nào cũng giống nhau nếu như cùng đời. Sẽ không có chuyện phần mềm trên máy này cài lên máy kia sẽ không chạy. Cũng không có chuyện cài phần mềm mới lên thì phần mềm cũ nào đó bị lỗi. Android mã nguồn mở, nhà sản xuất có quyền tùy chỉnh lõi kernel của nó nên chưa chắc phần mềm viết cho Android chạy trên điện thoại Samsung mà đưa lên điện thoại Android Sony thì chạy.

Các thư viện của Arduino cũng vậy. Tạm thời xem nó như phần mềm trên chiếc điện thoại Arduino. Chiếc điện thoại này có cấu hình phần cứng cùi bắp, chỉ thích hợp chạy đơn nhiệm chứ không phải đa nhiệm. Bạn cài lên nó hơn 1 phần mềm (#include hơn 1 thư viện) thì khả năng xảy ra xung đột đã có rồi đấy, đơn giản vì các thư viện được lập trình bởi những người khác nhau và không chắc chúng có dùng khác nền tảng phần cứng của Arduino hay không (Timer, Interrupt, PWM,...). Giả sử 2 thư viện dùng cùng phần cứng là Interrupt Pin Change chẳng hạn thì khả năng chúng "CẮN" nhau là 100% rồi. Trong một số trường hợp khác, thư viện chỉ hỗ trợ Arduino Mega 2560 chẳng hạn nhưng bạn dùng nó trên Uno thì cũng thua rồi.

## Những lưu ý khi sử dụng nhiều hơn 1 thư viện

Tất nhiên những trường hợp xung đột giữa các thư viện cũng không nhiều, và hầu như chỉ xảy ra khi dự án của bạn tương đối phức tạp xíu vì dùng nhiều thiết bị phần cứng khác nhau kết nối với Arduino, chứ không thì mọi người cũng nghỉ chơi với Arduino rồi. Mình nêu lên vấn đề này chủ yếu để các bạn không chuyên điện tử thì cũng nên để ý đến "note" có ghi trong thư viện, các nền phần cứng mà cái thư viện đó sử dụng, hay các chia sẻ cảnh báo xung đột thư viện từ cộng đồng. Vì nếu không, khi xảy ra lỗi, bạn có căng mắt tìm lỗi trong code mình viết thì cũng không ra đâu vì có thể nó ở thư viện. Rất nhiều trường hợp, các bạn copy code của nhau cho dự án robot không chạy được cũng do xung đột thư viện hoặc thư viện không hỗ trợ.

✨✨✨ Mình xin nêu bên dưới đây 3 trường hợp xung đột hoặc không hỗ trợ mà mình biết. Bạn nào có kinh nghiệm xương máu khác thì Share luôn để các bạn khác biết để không đâm đầu vào những tình huóng cắn lưỡi nha :)

1. SoftwareSerial vs Servo
2. IRRemote vs Tone
3. Pinchange vs SoftwareSerial
4. Không phải mọi chân của Arduino Mega hỗ trợ chân RX khi khai báo SoftwareSerial. Chi tiết bạn thâm khảo thông tin trong thư viện này.

Chúc các bạn né được càng nhiều càng tốt!
P/s: kiều gì thì cũng dính thôi, kkkk...
