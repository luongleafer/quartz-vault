---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 2
unit: 1
title: Phân tích phổ của tín hiệu liên tục
---
# Phân tích phổ của tín hiệu liên tục
Để nghiên cứu các tín hiệu phức tạp bất kì, ta cần phân tích tín hiệu đó thành tổ hợp tuyến tính của các tín hiệu đơn giản, như xung đơn vị, hoặc tín hiệu hình sin,...

## Phân tích phổ của tín hiệu liên tục tuần hoàn
Xét tín hiệu $x(t)$ liên tục theo thời gian $t$, tuần hoàn theo chu kì $T_p$, tần số $F_0 = \frac{1}{T_p}$, tần số góc $\omega_0 = \frac{2\pi}{T_p}$. Ta có thể chứng minh được, tín hiệu này có thể được tách thành tổng của các tín hiệu có dạng hình sin:
$$x(t) = \sum_{k=-\infty}^{\infty}c_ke^{j2\pi k F_0t}$$
Trong đó các hệ số $c_k$ được tính như sau:
$$c_k = \frac{1}{T_p}\int_{T_p}x(t)e^{-j2\pi k F_0t}dt$$
## Phân tích phổ của tín hiệu liên tục, không tuần hoàn
Ta đưa tín hiệu không tuần hoàn thành tín hiệu tuần hoàn tương ứng, với chu kì tiến tới vô cùng, khi đó ta có
Phương trình tổng hợp:
$$x(t) = \int_{-\infty}^\infty X(F)e^{j2\pi F t}dF$$
Phương trình phân tích
$$X(F) = \int_{-\infty}^{\infty}x(t)e^{-j 2\pi F t}dt$$
