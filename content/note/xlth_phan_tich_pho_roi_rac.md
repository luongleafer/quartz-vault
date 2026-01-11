---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 2
unit: 2
title: Phân tích phổ của tín hiệu rời rạc
---

# Phân tích phổ của tín hiệu rời rạc

## Phân tích phổ của tín hiệu rời rạc không tuần hoàn

Phép biến đổi Fourier cho tín hiệu rời rạc theo thời gian: (DTFT)
$$X(\omega) = \sum_{n=-\infty}^\infty x(n)e^{-jwn}$$
Phép biến đổi Fourier ngược cho tín hiệu rời rạc theo thời gian (IDTFT)
$$x(n) = \frac{1}{2\pi}\int_{-\pi}^{\pi}X(\omega)e^{jwn}d\omega$$
Ta có thể phân tích $X(\omega)$ thành hai thành phần, $|X(\omega)|$ được gọi là **phổ biên độ**, $\arg[X(\omega)] \in [-\pi;\pi]$, được gọi là **phổ pha**.
Ngoài ra ta có **phổ mật độ năng lượng**
$$S_{xx}(\omega) = |X(\omega)|^2$$

Một số tính chất của phép biến đổi Fourier
Tính tuyến tính:
$$ax_1(n) + bx_2(n) \xrightarrow{F} aX_1(\omega) + bX_2(\omega)$$
Tính tuần hoàn: $X(\omega)$ tuần hoàn với chu kì $2\pi$
Phép trễ: tín hiệu trễ $n_0$ mẫu, sau khi qua biến đổi Fourier sẽ có phổ biên độ không đổi, phổ pha lệch một lượng $\omega n_0$
$$F\{x(n-n_0)\} = e^{-j\omega n_0}X(\omega)$$
Phép tích chập qua biến đổi Fourier sẽ thành phép nhân thông thường
$$x(n) * h(n) \xrightarrow{F} X(\omega)H(\omega)$$
## Phép biến đổi Fourier rời rạc (DFT)
Phép biến đổi Fourier cho tín hiệu rời rạc cho ta một miền tần số liên tục. Phép biến đổi Fourier rời rạc sẽ trả về miền tần số rời rạc trên tần số độ dài hữu hạn
Biến đổi Fourier rời rạc:
$$X(k) = \begin{cases}
\sum_{n=0}^{N-1}{x(n)e^{-j \frac{2\pi}{N}nk}}\quad 0 \le k \le N-1 \\
0 \text{ với các k còn lại}
\end{cases}$$
Biến đổi Fourier ngược rời rạc:
$$x(n) = 
\begin{cases}
\frac{1}{N}\sum_{k=0}^{N-1}X(k)e^{j\frac{2\pi}{N}nk} \quad 0 \le n \le N-1 \\
0 \quad \text{n còn lại}
\end{cases}$$
## Phép biến đổi Fourier nhanh (FFT)
(todo)