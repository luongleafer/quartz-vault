---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 2
unit: 2
title: Đặc trưng của biến ngẫu nhiên
---
# Các đặc trưng của biến ngẫu nhiên
- Xét [[random_variable#Biến ngẫu nhiên|biến ngẫu nhiên]] $X$. Có hai loại đặc trưng của biến ngẫu nhiên:
	- Đặc trưng về trung tâm: Kỳ vọng, trung vị, mốt
	- Đặc trưng về độ phân tán: Phương sai và độ lệch chuẩn
## Kỳ vọng (expected value)
- Đối với biến ngẫu nhiên rời rạc, giá trị kỳ vọng là tổng của giá trị biến và xác suất biến nhận giá trị đó
$$E(X) = \mu = \sum_{i=1}^n{x_i p_i}$$
- Công thức trên có thể được áp dụng cho trường hợp biến ngẫu nhiên có vô hạn đếm được giá trị khả dĩ.
- Đối với biến ngẫu nhiên liên tục có hàm mật độ xác suất $f(x)$:
$$E(X) = \mu = \int_{-\infty}^{+\infty}{xf(x)\mathrm{d}x}$$
- Các tính chất của giá trị kỳ vọng:
	- $E(c) = c$ với $c$ là hằng số
	- $E(cX) = cE(X)$ với $c$ là hằng số
	- $E(X+Y) = E(X) + E(Y)$ với $X,Y$ là biến ngẫu nhiên
	- Nếu $X, Y$ [[cong_thuc_nhan_xac_suat#Sự kiện độc lập|độc lập]]: $E(XY) = E(X) E(Y)$
	- Nếu $Y = g(X)$ thì $E(Y) = \sum_i{g(x_i)p_i}$
## Mốt (modes)
- Là giá trị có của biến ngẫu nhiên mà tại đó, hàm mật độ xác suất có giá trị lớn nhất
## Trung vị (median)
- Là giá trị $m$ sao cho:
	- $P(X \le m)\ge 0,5$
	- $P(X \ge m) \ge 0,5$
## Phương sai (variance)
- Là giá trị đặc trưng cho độ phân tán của biến ngẫu nhiên, được tính bằng giá trị kỳ vọng của $(X - \mu)^2$
$$V(x) = \sigma^2 = E[(X-\mu)^2]$$
- Đối với biến ngẫu nhiên rời rạc, ta có
$$\begin{aligned}
V(x) &= E(X^2) -\mu^2 \\
&= \sum_{i}{x_i^2 p_i} - \bigg(\sum_i{x_ip_i}\bigg)^2 
\end{aligned}
$$
- **Độ lệch chuẩn (Standard deviation)** là căn bậc hai của phương sai
$$\sigma = \sqrt{V(x)}$$
