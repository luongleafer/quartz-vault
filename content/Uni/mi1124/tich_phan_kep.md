---
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 2
unit: 3
title: Tích phân kép
---

# Tích phân kép (Tích phân bội hai)

>[!question] Bài toán
>Tính thể tích khối trụ có đáy là miền $D \subset \mathbb{R}^2$, mặt trên là mặt cong có phương trình $z = f(x;y)$, các đường sinh song song với Oz. Kết quả của bài toán là một tích phân, được biểu diễn như sau:
>$$\iint_D{f(x;y) \, dx\, dy}$$

## Tính chất của tích phân kép
- Các công thức dưới đây viết gọn $f(x;y)$ thành $f$, $g(x;y)$ thành $g$. Các thành phần khác $f,g,x,y$ đều là các hằng số
- Tính tuyến tính:
$$\iint_D{(af + bg)\, dx\,dy} = a\iint_D{f\,dx\,dy} + b\iint_D{g\,dx\,dy}$$
- Tính phân hoạch: Chia $D$ thành n phần rời nhau, ta có:
$$\iint_D{f \, dx \,dy} = \sum_{i=1}^{n}{\iint_{D_i}{f \, dx \, dy}}$$
- Định lí giá trị trung bình

## Cách tính tích phân kép trong hệ tọa độ Descartes

>[!formula] Nếu $D$ có dạng hình chữ nhật $[a;b] \times [c;d]$ ta có:
>$$\iint_D{f\,dx\,dy} = \int_a^b{dx \int_c^d{f \, dy}} = \int_c^d{dy \int_a^b{f\, dx}}$$

>[!formula] Nếu $D$ bị chặn bởi $a\le x \le b$ và $y_1(x) \le y \le y_2(x)$
>$$\iint_D{f \, dx \, dy} = \int_a^b{dx \int_{y_1(x)}^{y_2(x)}{f\,dy}}$$

>[!formula] Nếu $D$ bị chặn bởi $c \le y \le d$ và $x_1(y) \le x \le x_2(y)$
>$$\iint_D{f \,  dx \, dy} = \int_c^d{dy \int_{x_1(y)}^{x_2(y)}{f\,dx}}$$

## Công thức đổi biến
Xét tích phân kép $\iint_D{f(x;y)\,dx\,dy}$. Thực hiện đổi biến
$$x = x(u;v), y = y(u;v)$$ với $(u;v) \in D'$ với các điều kiện sau:
- $x(u;v), y(u;v)$ _liên tục_, _có đạo hàm riêng_ trong miền $D'$
- Việc đổi biến xác định một _song ánh_ từ $D'$ lên $D$
- **Định thức Jacobi** $J = \begin{vmatrix}x'_u&x'_v\\ y'_u&y'_v\end{vmatrix} \neq 0$ trên $D$ hoặc chỉ bằng 0 tại một số điểm hữu hạn
Khi đó ta có:

>[!formula] Công thức đổi biến của tích phân kép
>$$\iint_D{f(x;y)\,dx \, dy} = \iint_{D'}{f(x(u;v);y(u;v)|J|\, du \, dv}$$

>[!formula] Công thức tích phân kép trong hệ tọa độ cực
>$$\iint_D{f(x;y)\, dx \, dy } = \iint_{D'}{f(r\cos\varphi;r\sin\varphi)r\, dr \, d\varphi}$$

## Ứng dụng
- Tính thể tích vật thể tạo bởi mặt cong $z_1(x;y)$ và $z_2(x;y)$($z_1\le z_2$) xác định trên miền D, các đường sinh song song Oz:
$$V = \iint_D{(z_2 - z_1)\,dxdy}$$
- Tính diện tích miền phẳng D:
$$S = \iint_D{dxdy}$$
- Tính diện tích mặt cong $z=z(x;y)$ có hình chiếu lên $Oxy$ là miền $D$:
$$S = \iint_D{\sqrt{1+z'_x + z'_y}\,dxdy}$$