---
layout: post
current: post
cover: https://i.ibb.co/yNXK0Gz/roblox-checkpoint-system.png
navigation: True
title: Tạo check point trong Obby game không cần code
date: 2020-05-29 10:00:00
tags: roblox
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

> Obby game của bạn đã khá dài và khó. Bạn muốn thêm cơ hội cho người chơi vượt qua thử thách của mình nhưng chưa biết lập trình roblox để tạo hệ thống checkpoint thì đây là bài viết bạn nên đọc.

![Checkpoint system in Obby game](https://d5m0vnpvja3z4.cloudfront.net/assets/blt3e7206e889f15cd9/IntroToStudio_heroCheckpoints.jpg)

## Tại sao cần hệ thống Checkpoint trong game Obby

Game Obby của bạn càng dài, càng nhiều chướng ngại vật thì cảm giác đau đớn cho người chơi khi gần đến đích mà lỡ bị ngã càng lớn. Trừ khi bạn muốn người chơi bỏ cuộc và không bao giờ chơi trò chơi của bạn nữa thì có thể chuyển sang đọc một nội dung khác ngay bây giờ. Còn nếu bạn muốn người chơi có sự phấn khích khi vượt qua thử thách của bạn và luôn sẵn sàng cho những thử thách khó hơn kế tiếp thì chắc chắn trò chơi của bạn cần có một hệ thống Checkpoint. Những điểm Checkpoint cho phép người chơi hồi sinh hay chơi lại sau khi vượt qua chướng ngại vật nào đó trong trò chơi của bạn.

Bạn nên đặt checkpoint tại những điểm sau trong trò chơi:

* Trước hoặc sau một bước nhảy khó khăn.
* Sau khi người chơi đã chơi vượt qua thử thách trong một khoảng thời gian nhất định (ngắn thôi).

<iframe width="560" height="315" src="https://www.youtube.com/embed/oit0emIg-4I" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Thiết lập hệ thống Checkpoint

Hệ thống Checkpoint có thể được thiết lập dễ dàng qua 9 bước bên dưới. Các bạn có thể tham khảo clip hướng dẫn để có thể dễ dàng hình dung cách làm hơn nhưng nên đọc qua các bước để hiểu ý nghĩa từng bước.

* Bước 1: Vào `Model > Gameplay > Spawn` để thêm các SpawnLocation (điểm hồi sinh) vào Obby Game của bạn.

![Create Spawn Location](https://i.ibb.co/s1qrCcB/Create-Spawn-Location.png)

* Bước 2: Đổi tên các Spawnlocation này theo tên gợi nhớ hoặc đánh số thứ tự để phân biệt.
* Bước 3: Vào `Model > Advanced > Service` và chọn Teams để thêm service này vào trò chơi.

![Insert Service](https://education.roblox.com/assets/bltedebb583f329051d/InsertService_updated.png)
![Team Insert](https://education.roblox.com/assets/blt8bc404f2f5e44057/TeamsInsert_480x320.png)

* Bước 4: Thêm các object Team vào Teams service.

![Team Created](https://education.roblox.com/assets/bltbd896d173e656933/TeamsCreated_480x320.png)
![Team Node](https://education.roblox.com/assets/blt80f34b39a099bd8b/TeamNode_480x320.png)

* Bước 5: Đổi tên các object Team này theo tên gợi nhớ hoặc đánh số thứ tự để phân biệt.

![Rename team Node](https://education.roblox.com/assets/blt828bd7894d85edf6/RenameTeamNode_480x320.png)

* Bước 6: Tạo liên kết giữa SpawnLocation object và Team object tương ứng thông qua thuộc tính TeamColor.
_**Một cặp SpawnLocation và Team tương ứng sẽ có cùng TeamColor. Các Team khác nhau thì TeamColor khác nhau.**_
* Bước 7: Tắt thuộc tính `Neutral` để ngăn nhân vật không hồi sinh ngẫu nhiên tại các điểm khác nhau.

![Uncheck Neutral](https://education.roblox.com/assets/blt2b5a63b09215b9d7/UncheckNeutral_480x320.png)

* Bước 8: Bật thuộc tính `AllowTeamChangeOnTouch` để ghi nhận sự thay đổi khi người chơi đến được một SpawnLocation mới (đổi Team).

![Spawn Location 2](https://education.roblox.com/assets/blt579cbd9c74250daf/SpawnLocation2_480x320.png)

* Bước 9: Bật thuộc tính `AutoAssignable` tại Team liên kết với SpawnLocation đầu tiên để thiết lập địa điểm mặc định khi người chơi bắt đầu trò chơi. Tắt `AutoAssignable` cho tất cả các Team còn lại.

![Team 2](https://education.roblox.com/assets/blt21a6db7158c8fd2d/Team2_480x320.png)

Chúc các bạn có thể hoàn thành Checkpoint System cho game Obby của mình.

> P/s: Bài viết tham khảo nguồn tại link: [Intro To Studio Checkpoints](https://education.roblox.com/en-us/resources/intro-to-studio-checkpoints). Nhưng đã có hiệu chỉnh lại thứ tự các bước thực hiện để người đọc dễ nắm hơn bản gốc.
