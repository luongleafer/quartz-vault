---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 2
unit: 4
title: Tích phân bội ba
share: true
---

# Tích phân bội ba
>[!question] Bài toán
>Tính khối lượng vật thể V không đồng chất có khối lượng riêng tại điểm $M(x;y;z)$ là $f(x;y;z)$
>$$\iiint_V{f(x;y;z)\,dxdydz}$$

## Tính chất
- Có đủ các tính chất của tích phân xác định và [[tich_phan_kep|Tích phân kép]]
## Cách tính trong hệ tọa độ Descartes
- Với miền V có dạng $[a;b] \times [c;d] \times [e;f]$
$$\iiint_V{f(x;y;z)\,dxdydz} = \int_a^b{dx}\int_c^d{dy}\int_e^f{f(x;y;z)\,dz}$$
- Với miền V có dạng: $a \le x \le b\,;\,y_1(x) \le y \le y_2(x)\,;\,z_1(x;y)\le z \le z_2(x;y)$, ta có:
$$\iiint_V{f(x;y;z)\,dxdydz} = \int_a^b{dx}\int_{y_1(x)}^{y_2(x)}{dy}\int_{z_1(x;y)}^{z_2(x;y)}{f(x;y;z)\,dz}$$

## Đổi biến
- Ta có phép đổi biến
$$\begin{cases}x = x(u,v,w)\\ y=y(u,v,w)\\ z=z(u,v,w)\end{cases}$$
và
$$J = \begin{vmatrix}x'_u && x'_v && x'_w\\ y'_u && y'_v && y'_w \\ z'_u && z'_v && z'_w \end{vmatrix} \neq 0$$
Xác lập miền $V_{uvw}$, ta có:

>[!formula] Công thức đổi biến tổng quát
>$$\iiint_V{f(x;y;z)\,dxdydz} = \iiint_{V_{uvw}}{f(x(u;v;w);y(u;v;w);z(u;v;w))}|J|\,dudvdw$$

>[!formula] Đổi biến tọa độ trụ
>$$\begin{cases}x = r\cos\varphi\\ y = r\sin\varphi \\ z = z\end{cases} \Rightarrow |J| = r$$

>[!formula] Đổi biến tọa độ cầu
>$$\begin{cases}x = r\sin\theta\cos\varphi \\ y = r\sin\theta\sin\varphi\\z=r\cos\theta\end{cases} \Rightarrow |J| = r^2\sin\theta$$
## 