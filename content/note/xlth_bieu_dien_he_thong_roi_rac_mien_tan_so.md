---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 2
unit: 3
title: Biểu diễn hệ thống rời rạc trên miền tần số
---
# Biểu diễn hệ thống rời rạc trên miền tần số
## Đáp ứng tần số của hệ thống tuyến tính bất biến rời rạc
Giả sử ta có hệ thống $y(n)$ có đáp ứng xung là $h(n)$, khi đó
$$
\begin{aligned}
y(n) = x(n) * h(n) = \sum_{k=-\infty}^\infty h(k)x(n-k)
\end{aligned}
$$
Giả sử tín hiệu đầu vào $x(n) = Ae^{j\omega_0n}$, khi đó:
$$
\begin{aligned}
y(n) &= \sum_{k=-\infty}^\infty h(k)x(n-k) \\
&= \sum_{k=-\infty}^\infty h(k)Ae^{j\omega_0(n-k)} \\
&= Ae^{j\omega_0n}\sum_{k=-\infty}^\infty h(k)e^{-j\omega_0 k} \\
&= Ae^{j\omega_0n}H(\omega_0)
\end{aligned}
$$
Trong đó $H(\omega)$ là [[xlth_phan_tich_pho_roi_rac|biến đổi Fourier]] của đáp ứng xung $h(n)$.
Như vậy, nếu ta phân tích được $x(n)$ thành tổng các tín hiệu hình sin dạng mũ phức, ta có thể tìm được $y(n)$ với mọi $x(n)$ qua $H(\omega)$ 
Ta có
$$H(\omega) = \sum_{-\infty}^\infty{h(k)e^{-j\omega k}} = H_R(\omega) + jH_I(\omega)$$
Khi đó
$$|H(\omega)|=\sqrt{H_R^2(\omega) + H_I^2(\omega)}$$ được gọi là **đáp ứng biên độ** của hệ thống trên miền tần số, và
$$\theta(\omega) = \tan^{-1}\frac{H_I(\omega)}{H_R(\omega)}$$ được gọi là **đáp ứng pha** của hệ thống trên miền tần số. Ta còn có thể biểu diễn $$H(\omega) = |H(\omega)|e^{j\omega\theta(\omega)}$$
Nếu $x(n)$ là tổng các hàm lượng giác, ví dụ
$$x(n) = \sum_{i=1}^{L}A_i\cos(\omega_i n + \varphi_i)$$
khi đó đáp ứng của hệ thống
$$y(n) = \sum_{i=1}^{L}A_i|H(\omega_i)|\cos(\omega_i n + \varphi_i + \theta(\varphi_i))$$
## Xác định đáp ứng tần số từ phương trình sai phân tuyến tính hệ số hằng
Giả sử hệ thống được cho bởi phương trình sai phân tuyến tính hệ số hằng:
$$\sum_{k=0}^N{a_ky(n-k)} = \sum_{k=0}^M b_kx(n-k)$$
Biến đổi Fourier hai vế, kết hợp với nhận xét $H(\omega) = \frac{Y(\omega)}{X(\omega)}$, ta có
$$H(\omega) = \frac{\sum_{k=0}^M b_k e^{-j\omega k}}{\sum_{k=0}^N a_k e^{-j\omega k}}$$

