---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 1
unit: 2
title: Ứng dụng của vi phân trong hình học không gian
share: true
---

# Ứng dụng của vi phân trong hình học không gian

## Hàm vector

>[!defintion] Định nghĩa
>Xét không gian 3 chiều $\mathbb{R}^3$ có cơ sở chính tắc ${\vec{i},\vec{j},\vec{k}}$
>Một **hàm vector** là một ánh xạ: $\vec{r}: \mathbb{R} \to \mathbb{R}^3; \vec{r}(t) = x(t)\vec{i} + y(t)\vec{j} +z(t)\vec{k} =(x(t);y(t);z(t))$ với $x(t), y(t),z(t)$ là các hàm một biến t trên $\mathbb{R}$

- Các định nghĩa về giới hạn, đạo hàm, tích phân tương tự như hàm một biến, trong đó:

>[!formula] Giới hạn, đạo hàm, tích phân của hàm vector
>Xét $t_0$ là một số hoặc $\pm \infty$. Ta có:
>$$\lim_{t\to t_0}{\vec{r}(t)} = (x_0;y_0;z_0) \Leftrightarrow \begin{cases}\lim_{t\to t_0}{x(t)} = x_0\\\lim_{t\to t_0}{y(t)} = y_0\\\lim_{t\to t_0}{z(t)} = z_0\end{cases}$$
>$$\vec{r}'(t) = (x'(t); y'(t);z'(t))$$
>$$\int{\vec{r}(t)\mathrm{d}t} = (\int x(t)\mathrm{d}t;\int y(t)\mathrm{d}t;\int z(t)\mathrm{d}t)$$

## Mặt cong trong không gian
- Xét mặt cong cho bởi phương trình tổng quát $F(x,y,z) = 0$. Tại điểm $M(x_0;y_0;z_0)$ là điểm chính quy, ta có **vector pháp tuyến của mặt cong tại M** là $\vec{n}_M = (F'_x(M);F'_y(M);F'_z(M))$
- **Tiếp diện** của mặt cong tại M là mặt phẳng đi qua M, lấy $\vec{n}_M$ là vector pháp tuyến
- **Pháp tuyến** của mặt cong tại M là đường thẳng đi qua M, lấy $\vec{n}_M$ là vector chỉ phương

## Đường cong trong không gian
- Xét đường cho bởi phương trình tham số:
$$(C) : \begin{cases}x = x(t)\\y=y(t)\\z=z(t)\end{cases}$$
	- Xét điểm $M$ ứng với $t = t_0$ là điểm chính quy, khi đó, xét **vector chỉ phương của đường cong tại M** $\vec{u}_M = (x'(t_0);y'(t_0);z'(t_0))$
- Xét đường cong là giao của hai mặt cong $(S_1) : F(x,y,z) = 0$ và $G(x,y,z) =0$ và điểm M(x_0;y_0;z_0) Gọi $\vec{n}_M^1$ là vector pháp tuyến của mặt cong $(S_1)$ tại $M$ và $\vec{n}_M^2$ là vector pháp tuyến của mặt cong $(S_2)$ tại $M$. Ta có $\vec{u}_M = [\vec{n}_M^1;\vec{n}_M^2]$
- **Tiếp tuyến** của đường cong tại M là đường thẳng qua M, lấy $\vec{u}_M$ làm vector chỉ phương
- **Pháp diện** của đường cong tại M là mặt phẳng đi qua M, lấy $\vec{u}_M$ làm vector pháp tuyến
- **Độ cong** của đường cong cho bởi phương trình tham số tại điểm $M$ ứng với $t = t_0$:
$$C_M = \frac{|[\vec{r}'(t_0) ; \vec{r}''(t_0)] |}{|\vec{r}'(t_0)|^3}$$