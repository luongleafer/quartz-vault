---
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 4
unit: 8
title: Tích phân đường
---

# Tích phân đường

## Loại I

- Bài toán: Tính khối lượng của dây không đồng chất $(C)$, biết mật độ vật chất tại điểm $M(x;y) \in (C)$ là $f(x;y)$ Kết quả của bài toán cho ta tích phân
$$I = \int_{(C)}{f(x;y)ds}$$
- Trong đó $ds$ được gọi là **vi phân cung**
- Tính chất:
	- Tuyến tính
	- Phân hoạch
	- Định lí giá trị trung bình
	- _Không phụ thuộc_ vào đường đi
- Cách tính: đưa về tích phân xác định

>[!formula] Tích phân đường loại I
>Với $(C)$ là đường cong cho bởi phương trình $y = y(x)$ và $a\le x \le b$ ta có
>$$I = \int_a^b{f(x;y(x))\sqrt{1 + (y'(x))^2}}\,dx$$
>Với $(C)$ là đường cong cho bởi phương trình tham số $x = x(t)$; $y = y(t)$ và $a \le t \le b$ ta có
>$$I = \int_a^b{f(x(t);y(t))\sqrt{[x'(t)]^2 + [y'(t)]^2}}\,dt$$

- Ứng dụng
>[!formula] Độ dài đường cong $(C)$
>$$L = \int_{(C)}{ds}$$

## Loại II
- Xét lực $\vec{F}(x;y) = P(x;y)\vec{i} + Q(x;y)\vec{j}$ là một lực biến đổi liên tục trên $\mathbb{R}^2$. Công do lực thực hiện để di chuyển chất điểm dọc theo đường cong $(C)$ là tích phân

$$I = \int_{(C)}{P(x;y)\,dx + Q(x;y)\,dy}$$
- Tính chất
	- Tuyến tính
	- Phân hoạch
	- Định lí giá trị trung bình
	- _Phụ thuộc_ vào điểm đầu và điểm cuối

$$\int_{AB}{Pdx + Qdy} = - \int_{BA}{Pdx + Qdy}$$
- Cách tính
>[!formula] Tích phân đường loại II
>Nếu cung $AB$ cho bởi đường $y = y(x)$
>$$I = \int_{x_A}^{x_B}{[P(x;y(x)) + Q(x;y(x))y'(x))]\,dx}$$
>Nếu cung $AB$ cho bởi phương trình tham số $x = x(t)$, $y = y(t)$
>$$I = \int_{t_A}^{t_B}{[P(x(t);y(t))x'(t)  + Q(x(t);y(t))y'(t) ]\,dt}$$

## Công thức Green
- Cho miền $D$ liên thông, bị chặn có biên là $L$ gồm một/nhiều đường con kín trơn từng khúc, rời nhau đôi một, $P(x;y)$ và $Q(x;y)$, các đạo hàm riêng cấp một liên tục trong $D$, ta có

>[!formula] Công thức Green
>$$\int_L{Pdx + Qdy} = \iint_{D}{\bigg(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\bigg)\,dxdy }$$

## Điều kiện để tích phân không phụ thuộc đường đi

>[!formula] 4 mệnh đề tương đương
>$$Q'x = P'y\, \forall (x;y) \in D$$
>$$\oint_L{Pdx + Qdy} = 0$$ với mọi đường cong kín, trơn từng khúc $L$ trong $D$
>$$\int_{AB}{Pdx + Qdy}$$ chỉ phụ thuộc vào điểm đầu A, điểm cuối B mà không phụ thuộc vào đường đi giữa hai điểm đó
>$$Pdx + Qdy$$ là _vi phân toàn phần_ của một hàm $u(x;y)$ nào đó trong miền $D$


Một số hệ quả:
- Khi đó
$$u(x;y) = \int_{x_0}^x P(t,y_0)\,dt + \int_{y_0}^y{Q(x, t)\,dt} + C$$  hoặc
$$u(x;y) = \int_{y_0}^{y}Q(x_0,t)\,dt + \int_{x_0}^x{P(t, y)dt} + C$$

và 
$$\int_{AB} = Pdx + Qdy = u(B) - u(A)$$

