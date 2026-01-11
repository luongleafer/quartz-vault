---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 2
unit: 3
title: Các phân phối xác suất thường gặp
---
# Các phân phối xác suất quan trọng
- Xét $X$ là [[random_variable|biến ngẫu nhiên rời rạc]]
- Mục này phân tích một số phân phối xác suất thường gặp và các [[random_variable_characteristic|đặc trưng]] của chúng.
## Phân phối đều (uniform distribution)
- Là phân phối xác suất mà xác suất tại mỗi giá trị có thể nhận được là _như nhau_
$$p_i = P(X = x_i) = \frac{1}{n}$$
## Phân phối Bernoulli
- Phân phối Bernoulli biểu diễn phân phối xác suất tương ứng với một phép thử Bernoulli.
- Xét một phép thử chỉ có hai kết cục, sự kiện $A$ xảy ra với xác suất $p$, hoặc sự kiện $A$ không xảy ra.
- Xét $X$ là biến ngẫu nhiên rời rạc sao cho:
	- $X = 0$  nếu $A$ không xảy ra
	- $X = 1$ nếu $A$ xảy ra
- Phân phối xác suất của $X$ được cho trong bảng sau

$$
\begin{array}{c|c|c}
X & 0 & 1 & \\
\hline
P & 1-p & p 
\end{array}
$$
- Ta có
	- $E(X) = p$
	- $V(X) = p(1-p)$
## Phân phối nhị thức (Binomial Distribution)
- Xét $n$ phép thử độc lập, giống nhau, mỗi phép thử có xác suất $p$ thành công.
- Gọi $X$ số lần thành công trong $n$ phép thử. $X$ là biến ngẫu nhiên rời rạc, nhận $n+1$ giá trị từ $0$ đến $n$.
- $X$ có phân phối nhị thức với hai tham số $n$ và $p$, kí hiệu $B(n;p)$ 
- Áp dụng [[bernoulli_formula|Công thức Bernoulli]] ta có
$$P(X=k) = C^k_n p^k(1-p)^{n-k}$$
- Phía trên là hàm xác suất của biến ngẫu nhiên rời rạc $X$.
- Ta có 
	- $E(X) = np$
	- $V(X) = np(1-p)$
	- Mốt:
		- $np-q$ hoặc $np-q+1$ nếu $np-q \in \mathbb{Z}$
		- $\lfloor np-q\rfloor +1$ nếu $np-q \notin \mathbb{Z}$
## Phân phối Poisson
- Gọi $\lambda$ là số lần trung bình sự kiện  xảy ra trong một khoảng thời gian.
- Gọi $X$ là số lần xảy ra sự kiện $A$ trong khoảng thời gian đó.
- $X$ là biến ngẫu nhiên rời rạc, có thể nhận một số vô hạn đến được các giá trị.
- $X$ có phân phối xác suất Poisson với tham số $\lambda$, kí hiệu $P(\lambda)$
- Hàm xác suất của $X$:
	- $p_x = P(X= x) = e^{-\lambda}\frac{\lambda^x}{x!}$
- Ta có
	- $E(X) = V(X) = \lambda$
	- Mốt
		- $\lambda - 1$ hoặc $\lambda$ nếu $\lambda \ \in \mathbb{Z}$
		- $[\lambda - 1] + 1$ nếu $\lambda \notin \mathbb{Z}$

## Phân phối chuẩn (Normal Distribution)
- Là phân phối tương đối quan trọng, thường dùng để mô hình hóa các biến ngẫu nhiên trong tự nhiên khi chưa biết phân phối của chúng.
- Một biến ngẫu nhiên tuân theo phân phối chuẩn với tham số $\mu$ và $\sigma$ , kí hiệu $N(\mu,\sigma^2)$ có hàm mật độ xác suất như sau
$$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
- Các đặc trưng:
	- $E(X) = Med(X) = Mode(X) = \mu$
	- $V(X) = \sigma^2$
- Nếu $\mu = 0$ và $\sigma = 1$, ta có **phân phối chuẩn tắc** $N(0;1)$, hàm mật độ xác suất của phân phối chuẩn tắc là
$$\varphi(x) = \frac{1}{\sqrt{2\pi}}e^{\frac{-x^2}{2}}$$
- Mọi biến ngẫu nhiên tuân theo phân phối chuẩn đều có thể đưa về dạng chuẩn tắc, thật vậy, nếu $X$ tuân theo phân phối chuẩn $N(\mu,\sigma^2)$ thì $Z = \frac{X-\mu}{\sigma}$ tuân theo phân phối chuẩn tắc.
- Hàm phân phối xác suất
$$\Phi(t) = P(Z < t) = \int_{-\infty}^t(f(x)dx) = \int_{-\infty}^t {\frac{1}{\sqrt{2\pi}}e^{\frac{-x^2}{2}}}dx$$
- Nhận xét:
$$\Phi(t) = \frac{1}{2}+\int_0^t{\frac{1}{\sqrt{2\pi}}e^{\frac{-x^2}{2}}}dx = \frac{1}{2}+\phi(t)$$
- Tính chất của các hàm:
	- $\varphi(t)$ là hàm chẵn
	- $\phi(t)$ là hàm lẻ
	- $\Phi(t) + \Phi(-t) = 1$
- Quy tắc 3-sigma:
	- $P(|X-\mu|<\sigma) \approx 68,26\%$
	- $P(|X-\mu| < 2\sigma) \approx 95,44 \%$
	- $P(|X-\mu|<3\sigma)\approx 99,74\%$

## Xấp xỉ phân phối nhị thức
- Xét phân phối nhị thức $B(n;p)$.
	- Nếu $n$ lớn và $p$ nhỏ, $B(n;p)$ xấp xỉ $P(np)$
	- Nếu $n$ lớn và $p$ gần $0,5$, $B(n;p)$ xấp xỉ $N(np,npq)$