---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 2
unit: 1
title: Biến ngẫu nhiên
---
# Biến ngẫu nhiên
## Khái niệm

>[!definition] Biến ngẫu nhiên
>Xét một [[phep_thu_su_kien|phép thử ngẫu nhiên]] có không gian mẫu $\Omega$. Biến ngẫu nhiên là một phép gán mỗi kết cục sơ cấp cho một số thực, tức là ánh xạ
>$$\begin{aligned}X: \Omega &\to \mathbb{R} \\ \omega &\mapsto X(\omega) \end{aligned}$$

- Biến ngẫu nhiên rời rạc là biến ngẫu nhiên mà tập giá trị của nó là _hữu hạn_ hoặc _vô hạn đếm được_.
- Biến ngẫu nhiên liên tục là biến ngẫu nhiên mà tập giá trị của nó lấp kín một khoảng trên trục số, tức là đoạn $[a;b] \subset \mathbb{R}$ hoặc toàn bộ $\mathbb{R}$

## Phân phối xác suất của biến ngẫu nhiên
- Là một bảng/hàm số/đồ thị cho biết:
	- biến $X$ nhận giá trị nào
	- xác suất để $X$ nhận từng giá trị
- Bảng phân phối xác suất có dạng:
$$
\begin{array}{c|c c c c|c}
x & x_1 & x_2 & \dots & x_n & \\
\hline
p & p_1 & p_2 & \dots & p_n
\end{array}
$$
- Trong đó:
	- $p_i = P(X= x_i)$
	- $0 < p_i \le 1$
	- $\sum_{i=1}^n{p_i} = 1$
- Hàm (mật độ) xác suất là hàm số thể hiện xác suất của từng giá trị $x$
$$p(x) = P(X = x_i)$$
## Hàm phân phối xác suất
- là hàm $$F_X(x) = P(X < x), x \in \mathbb{R}$$
- Với biến ngẫu nhiên rời rạc
$$F_X(x) = \sum_{t<x} P(X=t)$$

- Hàm PPXS có các tính chất sau:
	- $0 \le F_X(x) \le 1$
	- Hàm $F_X(x)$ là hàm _không giảm_
	- $\lim_{x \to +\infty}{F_X(x)} = 1$
	- $\lim_{x \to - \infty}{F_X(x)} = 0$
	- $P(a \le x < b) = F_X(b) - F_X(a)$
