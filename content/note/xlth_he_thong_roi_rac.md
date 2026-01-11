---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 1
unit: 4
title: Hệ thống xử lí tín hiệu rời rạc
---
# Hệ thống xử lí tín hiệu rời rạc

Một **hệ thống** là bất cứ thiết bị nào có thể chuyển đổi tín hiệu này sang tín hiệu khác. Xét một hệ thống $T$. Khi ta đưa tín hiệu $x(n)$ vào $T$, ta nhận được một tín hiệu khác, kí hiệu $y(n) = T[x(n)]$.
## Một số tính chất của hệ thống
### Tính tuyến tính
Một hệ thống được gọi là tuyến tính nếu
$$T[ax_1(n) + bx_2(n)] = aT[x_1(n)] + bT[x_2(n)]$$
Khi làm việc với hệ tuyến tính, ta có thể phân tích đầu vào thành tổ hợp tuyến tính của nhiều tín hiệu nhỏ, đưa từng tín hiệu nhỏ qua hệ thống, rồi kết hợp lại để tìm được đầu ra.
### Tính bất biến
Một hệ thống được gọi là bất biến với thời gian (time-invariant), gọi tắt là bất biến nếu đầu vào bị trễ $k$ mẫu, thì đầu ra cũng trễ $k$ mẫu, hay
$$
T[x(n-k)] = T[x](n-k)$$
### Đáp ứng xung của hệ thống
**Đáp ứng xung (impulse response)** của một hệ thống, là đầu ra của hệ thống với đầu vào là [[xlth_tin_hieu_roi_rac#Một số tín hiệu rời rạc cơ bản|xung đơn vị]]
$$h(n) = T[\delta(n)]$$
## Hệ thống tuyến tính bất biến.
### Tính chất của hệ thống tuyến tính bất biến

Ta có nhận xét: mọi tín hiệu rời rạc đều có thể được tách thành tổng của các [[xlth_tin_hieu_roi_rac#Phân tích tín hiệu|xung đơn vị với độ trễ khác nhau]], hay
$$x(n) = \sum_{k = -\infty}^\infty x(k) \delta(n-k)$$
Trong đó, ở vế phải của phương trình trên, $x(k)$ là giá trị của tín hiệu tại mẫu thứ $k$.
Khi đưa tín hiệu trên vào một hệ thống tuyến tính bất biến, ta có
$$T[x(n)] = \sum_{k = -\infty}^{\infty}x(k)T[\delta(n-k)] = \sum_{k = -\infty}^\infty{x(k)h(n-k)}$$
Như vậy, nếu ta biết đáp ứng xung của hệ thống, và hệ thống đó là tuyến tính bất biến, ta có thể biết được tín hiệu ra của _mọi_ tín hiệu vào:
$$y(n) = \sum_{k = -\infty}^\infty{x(k)h(n-k)}$$
Ta định nghĩa phép tính trên là phép **tích chập (convolution)** giữa hai tín hiệu $x(n)$ và $h(n)$, kí hiệu $x(n) * h(n)$

### Tính chất của phép tích chập
Tính giao hoán
$$x(n) * h(n) = h(n) * x(n)$$
Tính kết hợp
$$[x(n)*h_1(n)]*h_2(n) = x(n) * [h_1(n)*h_2(n)]$$
Ý nghĩa: một tín hiệu được đưa liên tiếp qua hai hệ thống, có thể được thay bằng một hệ thống tương đương có đáp ứng xung là tổng chập của hai hệ thống ban đầu
![[Pasted image 20251203165206.png]]

Tính phân phối với phép cộng thông thường
$$x(n)*[h_1(n)+h_2(n)] = x(n)*h_1(n) + x(n) * h_2(n)$$
Ý nghĩa: nếu một tín hiệu được đưa qua hai hệ thống một cách độc lập rồi lấy tổng, có thể thay bằng một hệ thống tương đương có đáp ứng xung là tổng đáp ứng xung của hai hệ thống ban đầu. Ngoài ra, một hệ thống phức tạp cũng có thể được phân tích thành nhiều hệ thống nhỏ, đưa tín hiệu qua từng hệ thống rồi công lại.
![[Pasted image 20251203165308.png]]

## Tính nhân quả và ổn định của hệ thống
### Tính nhân quả
Một hệ thống được gọi là một **hệ thống nhân quả** nếu tín hiệu đầu ra _chỉ phụ thuộc vào đầu vào ở hiện tại và quá khứ_, tức là
$$y(n) = \sum_{k=0}^\infty a_kx(n-k)$$
Nếu hệ thống có đầu ra phụ thuộc vào đầu vào trong tương lai, hệ được gọi là không nhân quả. Chỉ có hệ nhân quả là khả thi trong thực tế.

Đáp ứng xung của hệ thống nhân quả $h(n) =0 \quad \forall n < 0$

### Tính ổn định
Một hệ thống được gọi là ổn định nếu với tín hiệu đầu vào bị chặn, tín hiệu đầu ra cũng bị chặn.
Hệ thống ổn định giúp ngăn chặn tình trạng tràn số (overflow) và các biểu hiện bất thường
Một hệ thống ổn định khi và chỉ khi
$$\sum_{k=-\infty}^\infty|h(k)| < \infty$$
