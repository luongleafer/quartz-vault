---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 3
unit: 2
title: Mẫu ngẫu nhiên và Phân phối mẫu
---
# Mẫu ngẫu nhiên và phân phối mẫu

## Mẫu ngẫu nhiên và thống kê
Giả sử ta khảo sát tính chất $X$ của [[mi2021_tong_the_va_mau|tổng thể]]. $X$ là một [[random_variable|biến ngẫu nhiên]] có phân phối xác suất $F_X(x)$. Khi đó, phân phối xác suất của $X$ được gọi là phân phối xác suất của tổng thể. Các đặc trưng $\mu = E(X)$ và $\sigma^2 = V(X)$ lần lượt được gọi là **trung bình (kỳ vọng) tổng thể** và **phương sai tổng thể**.

Một **mẫu ngẫu nhiên** có kích thước $n$ là tập hợp $n$ biến ngẫu nhiên $W_X = (X_1; X_2; ...; X_n)$ có _cùng phân phối xác suất_ với $X$.
Khi mỗi biến ngẫu nhiên từ $X_1$ đến $X_n$ nhận được giá trị cụ thể, ta có một _mẫu_ $(x_1; x_2; ...; x_n)$.

Một **thống kê** là một hàm của mẫu ngẫu nhiên:
$$\hat{\Theta} = g(X_1; X_2; ... ; X_n)$$
Như vậy, một thống kê cũng là một biến ngẫu nhiên. Khi mẫu ngẫu nhiên nhận giá trị cụ thể, thống kê cũng có giá trị cụ thể, $\hat{\theta} = g(x_1; x_2; ...; x_n)$.

## Một số thống kê thường gặp
Giả sử $X$ có kỳ vọng $E(X) =\mu$ và phương sai $V(X) = \sigma^2$.
**Trung bình mẫu ngẫu nhiên** là một thống kê, kí hiệu là $\bar{X}$, được định nghĩa như sau:
$$\overline{X} = \frac{1}{n} \sum_{i=1}^n X_i$$
Khi mẫu nhận giá trị cụ thể, trung bình mẫu ngẫu nhiên $\overline{X}$ nhận giá trị cụ thể là $\overline{x}$.
Kỳ vọng và phương sai của trung bình mẫu ngẫu nhiên:

$$E(\overline{X}) =\mu\quad V(\overline{X}) = \frac{\sigma^2}{n}$$
**Phương sai mẫu ngẫu nhiên** là một thống kê, kí hiệu là $\hat{S}^2$, được định nghĩa như sau:
$$\hat{S}^2 = \frac{1}{n}\sum_{i = 1}^n{(X_i - \overline{X})^2}$$
Khi mẫu nhận giá trị cụ thể, phương sai mẫu ngẫu nhiên $\hat{S}^2$ nhận giá trị cụ thể là $\hat{s}^2$.
Kỳ vọng của phương sai mẫu nhiên
$$E(\hat{S}^2) = \frac{n-1}{n}\sigma^2$$
**Độ lệch chuẩn mẫu ngẫu nhiên** là một thống kê, kí hiệu là $\hat{S}$, là căn bậc hai số học của phương sai.

Nếu dấu hiệu ta cần khảo sát là một dấu hiệu định tính, và ta cần thống kê số phần tử có tính chất đó, ta sử dụng biến ngẫu nhiên $X$ có [[common_probability_distribution#Phân phối Bernoulli|phân phối Bernoulli]] với tham số $p$ là tỉ lệ số cá thể trong tổng thể có tính chất đó so với kích thước tổng thể.
Khi đó, **tần suất mẫu ngẫu nhiên** là một thống kê, kí hiệu là $\hat{P}$. Dễ thấy $\hat{P} = E(X)$
Khi đó, kì vọng và phương sai của tần suất mẫu ngẫu nhiên:
$$E(\hat{P}) = p \quad V(\hat{P}) = \frac{p(1-p)}{n}$$
## Phân phối mẫu
Phân phối xác suất của một thống kê được gọi là **phân phối mẫu**.
