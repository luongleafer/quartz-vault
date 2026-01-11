---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 4
unit: 1
title: Biến đổi Z
---
# Biến đổi Z
## Khái niệm và miền hội tụ
Biến đổi Z (Z-transform) là một dạng biểu diễn khác của tín hiệu trong miền số phức, theo đó, tín hiệu $x(n)$ có biến đổi z là $X(z)$ với
$$X(z) = \sum_{n=-\infty}^\infty{x(n)z^{-n}}$$
Các giá trị $z$ để $X(z)$ hội tụ được gọi là **miền hội tụ (region of convergence)** của $X(z)$.
Đối với tín hiệu hữu hạn:
- Nếu là tín hiệu nhân quả: miền hội tụ là $z \neq 0$
- Nếu là tín hiệu phản nhân quả: miền hội tụ là $z \neq \infty$
Đối với tín hiệu vô hạn, để xác định miền hội tụ, ta có thể áp dụng tiêu chuẩn Cauchy, cụ thể, đặt
$$R_{x-} = \lim_{n\to \infty}|x(n)|^\frac{1}{n}; R_{x+} = \frac{1}{\lim_{n\to \infty}|x(-n)|^\frac{1}{n}}$$ thì miền hội tụ của $X(z)$ là $0 \le R_{x-} < |z| < R_{x+} \le \infty$.
Ví dụ, với tín hiệu $x(n) = a^n u(n)$, ta có: phép biến đổi z:
$$X(z) = \frac{z}{z-a}$$ với miền hội tụ là $|z| > |a|$
Nhận xét: tín hiệu có chiều dài vô hạn trên miền thời gian có thể được biểu diễn một cách hữu hạn trên miền z dưới dạng thương của hai đa thức của z.
Kí hiệu cho phép biên đổi z: $x(n) \xrightarrow{z} X(z)$
## Các tính chất của phép biến đổi z
**Tính tuyến tính**: nếu $X_1(z)$ là biến đổi z của $x_1(n)$, $X_2(z)$ là biến đổi z của $x_2(n)$ thì
$$ax_1(n) + bx_2(n) \xrightarrow{zt} a X_1(z) + bX_2(z)$$
và miền hội tụ của $X(z)$ là giao hai miền hội tụ của $X_1(z)$ và $X_2(z)$.

**Tính chất trễ**: nếu $X(z)$ là biến đổi $z$ của $x(n)$ thì
$$x(n-n_0) \xrightarrow{zt} z^{-n_0}X(z)$$
(miền hội tụ không thay đổi)
Từ đó ta có
$$a^{n-1}u(n-1) \xrightarrow{zt} \frac{1}{z-a}$$
**Scaling**:
$$a^nx(n) \xrightarrow{zt} X(a^{-1}z)$$
Nếu $X(z)$ có miền hội tụ $r_1 < |z| < r_2$ thì $X(a^{-1}z)$ có miền hội tụ là $|a|r_1 < |z| < |a|r_2$. Phép scaling có thể làm mở rộng/thu hẹp miền hội tụ.

**Đảo trục thời gian**
$$x(-n) \xrightarrow{zt} X(\frac{1}{z})$$
miền hội tụ $\frac{1}{z_2} < |z| < \frac{1}{z_1}$

**Vi phân của biến đổi z**:
$$nx(n) \xrightarrow{zt} -z\frac{\partial X(z)}{\partial z}$$
**Biến đổi z của tổng chập**:
$$x(n) * h(n) \xrightarrow{zt} X(z)H(z)$$

## Biến đổi z ngược
Từ miền z ta có thể thu được tín hiệu trên miền thời gian qua biến đổi z ngược. Nếu tín hiệu có dạng là thương của hai đa thức, ta có thể tách thành các đa thức dạng $\frac{z}{z-a}$ hoặc $\frac{1}{z-a}$
