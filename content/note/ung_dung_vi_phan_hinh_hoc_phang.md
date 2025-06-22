---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
subject-code: mi1124
chapter: 1
unit: 1
title: Ứng dụng của vi phân trong hình học phẳng
share: true
---

# Ứng dụng của vi phân trong hình học phẳng

## Tiếp tuyến, pháp tuyến của đường cong phẳng

- Cho một đường cong $\mathcal{C}$ và một điểm $M$
- Đường thẳng _chỉ cắt đường cong tại $M$_ được gọi là **tiếp tuyến** của đường cong tại $M$
- Đường thẳng _vuông góc_ với tiếp tuyến tại $M$ được gọi là **pháp tuyến** của đường cong tại $M$
- Nếu gọi vector chỉ phương của đường tiếp tuyến là $\vec{u}_M$ thì $\vec{u}_M$ là vector pháp tuyến của đường pháp tuyến. Vector này được gọi là **vector tiếp tuyến** của $\mathcal{C}$ tại $M$
- Nếu gọi vector chỉ phương của đường pháp tuyến là $\vec{n}_M$ thì $\vec{n}_M$ là vector pháp tuyến của đường tiếp tuyến. Vector này được gọi là **vector pháp tuyến** của $\mathcal{C}$ tại $M$

>[!caution] Chú ý
>$$\vec{u}_M \perp \vec{n}_M \forall M \in \mathcal{C}$$

>[!formula] Công thức tìm vector tiếp tuyến, vector pháp tuyến
>Nếu đường cong $\mathcal{C}$ được xác định từ hàm số $F(x,y) = 0$. M được gọi là **điểm chính quy** nếu $(F'_x(M))^2 + (F'_y(M))^2 \neq 0$. Khi đó ta có:
>$$\vec{n}_M = (F'_x(M); F'_y(M))$$
>Nếu đường cong $\mathcal{C}$ được xác định dưới dạng tham số $x = x(t); y= y(t)$. M ứng với tham số $t_M$. M được gọi là **điểm chính quy** nếu $(x'(t_M))^2 + (y'(t_M))^2 \neq 0$.
>Khi đó ta có:
>$$\vec{u}_M = (x'(t_M); y'(t_M))$$


## Độ cong của đường cong tại một điểm

>[!formula] Với đường cong cho dưới dạng tham số
>Cho $\mathcal{C} : \begin{cases}x = x(t)\\y = y(t)\end{cases}$ và điểm chính quy $M$ ứng với $t = t_0$. Độ cong:
>$$K_M = \frac{ |x'(t_0).y''(t_0) - x''(t_0)y'(t_0)|}{[(x'(t_0))^2 + (y'(t_0))^2]^\frac{3}{2}}$$

>[!formula] Với đường cong cho dưới dạng hàm số
>Cho $\mathcal{C} : y = y(x)$ và điểm chính quy $M$ ứng với $x = x_0$. Độ cong:
>$$K_M = \frac{|y''(x_0)|}{[1+ (y'(x_0))^2]^\frac{3}{2}}$$

>[!formula] Với đường cong trong tọa độ cực
>Cho $\mathcal{C} : r = r(\varphi)$ và điểm $M$ ứng với $\varphi = \varphi_0$. Độ cong:
>$$K_M = \frac{r^2 + 2(r'(\varphi))^2 - r.r''(\varphi)}{[r^2 + (r'(\varphi))^2]^\frac{3}{2}}$$

## Hình bao của họ đường cong
- Cho họ đường cong $\mathcal{C}: F(x,y,c) = 0$. Một đường cong $\mathcal{L} : G(x,y) = 0$ được gọi là **hình bao** của họ đường cong trên nếu:
	- Mọi đường cong của $\mathcal{C}$ tiếp xúc với $\mathcal{L}$
	- Với mọi điểm thuộc $\mathcal{L}$, ta luôn tìm được một đường thuộc $\mathcal{C}$ tiếp xúc với $\mathcal{L}$ tại điểm đó

>[!formula] Phương pháp tìm hình bao của họ đường cong
>Cho họ đường cong $\mathcal{C}: F(x,y,c) = 0$. Để tìm hình bao:
>- Tìm các điểm kì dị của họ đường cong
>- Giải hệ 
>$$
>\begin{cases}
>F(x,y,c) = 0\\
>F'_c(x,y,c) = 0
>\end{cases}
>$$
>- Việc giải hệ sẽ đưa đến một phương trình dạng $G'(x,y) = 0$. Loại quỹ tích các điểm kì dị khỏi phương trình này, ta được hình bao của họ đường cong là $G(x,y) = 0$