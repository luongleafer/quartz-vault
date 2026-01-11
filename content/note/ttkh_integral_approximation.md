---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 5
unit: 2
title: Tính gần đúng tích phân
---
# Tính gần đúng tích phân
## Phương pháp Newton-Cotes
- Để tính $\int{f(x)dx}$, ta [[ttkh_line_fitting#Nội suy Lagrange|nội suy]] hàm $f(x)$ bằng đa thức bằng nội suy lagrange
$$
\begin{aligned}
\int_a^bf(x)dx &= \int_a^b\bigg(\sum_{i = 0}^m \prod_{j = 0, j\neq i}^m \frac{x-x_j}{x_i-x_j}f(x_i)\bigg)dx \\
&= \sum_{i = 0}^mf(x_i)\int_a^b\bigg(\prod_{j = 0, j \neq i}^m\frac{x-x_j}{x_i - x_j}\bigg)dx
\end{aligned}
$$

## Các công thức
- Công thức hình thang: $m=1$, nội suy bằng đa thức bậc nhất
$$I = \frac{f(a) + f(b)}{2}(b-a)$$
	- Sai số: $$-\frac{b-a}{12}f''(c)h^2\quad c \in [a;b], h = b - a$$
	- Mở rộng: khia thành $n$ khoảng bằng nhau có độ dài $h = \frac{b-a}{n}$ bằng $n+1$ điểm $x_i = a + ih \quad (0 \le i \le n)$, mỗi khoảng đều dùng nội suy tuyến tính, ta có: $$I = \frac{h}{2}\bigg[f(a) + 2 \sum_{i=1}^{n-1}f(a+ih) + f(b)\bigg]$$
- Công thức Simpson 1/3: $m =2$, nội suy bằng đường parabol, với $h = (b-a)/2$
$$I = \frac{h}{3}[f(a)+4f(a + h) + f(b)]$$
	- Mở rộng: chia thành một số $n$ (chẵn) khoảng con bằng $n+1$ điểm từ $x_0$ đến $x_{2n}$, mỗi khoảng có độ dài $h = (b-a)/n$, ta có $$I = \frac{h}{3}\bigg[f(x_0) + 4\sum_{i=1}^{\frac{n}{2}}f(x_{2i-1}) + 2 \sum_{i = 1}^{\frac{n}{2}-1} f(x_{2i}) + f(x_n)\bigg]$$
- Công thức Simpson 3/8: $m = 3$, với $h = (b-a)/3$
$$I = \frac{3h}{8}[f(a) + 3f(a+h) + 3f(a+2h) + f(b)]$$
