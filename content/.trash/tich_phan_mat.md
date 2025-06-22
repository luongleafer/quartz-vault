---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 5
unit: 9
title: tich_phan_mat
share: true
---

## Tích phân mặt loại I
- Xét bài toán: tính khối lượng của mặt cong, trơn $S$, biết mật độ khối lượng của mặt cong tại điểm $M(x;y;z)$ là $f(x;y;z)$. Kết quả của bài toán cho ta tích phân mặt loại I:

$$\iint_{S}{f(x;y;z)dS}$$

- Với $dS$ là **vi phân mặt**, nếu mặt $S$ cho bởi phương trình $z = z(x;y)$ thì $dS = \sqrt{1+{z'}_x^2 + {z'}_y^2}dxdy$
- Cách tính: đưa về [[tich_phan_kep|tích phân kép]]
	- Xác định _phương trình_ mặt $S$: $z = z(x;y)$
	- Xác định _hình chiếu_ của mặt $S$ lên $Oxy$ là $D$
	- $z(x;y)$ và các đạo hàm riêng liên tục trên $D$, ta có

$$\iint_S{f(x;y;z)dS} = \iint_D{f(x;y;z(x;y))}dxdy$$

## Tích phân mặt loại II
### Tính định hướng của mặt gắn với vector pháp tuyến
### Định nghĩa, tính chất
- Cho mặt cong $S$ nằm trong chất lỏng đang chảy với mặt độ $\rho(x;y;z)$ và vận tốc $\vec{v}(x;y;z)$. Tính lượng chất lỏng chảy qua mặt cong trong một đơn vị thời gian
- Tích phân mặt loại II của $\vec{F}(P;Q;R)$ theo hướng $d\vec{a}$ của $S$ là

$$\iint_S{Pdydz + Qdzdx + Rdxdy}$$
### Cách tính: tính trực tiếp
- Ví dụ cần tính $\iint_S{Rdxdy}$ . 
- Viết $S$ dưới dạng $z = z(x;y)$
- Gọi $D$ là hình chiếu của $S$ trên $Oxy$
- Ta có

$$\iint_S{Rdxdy} = \iint_D{R(x;y;z(x;y))dxdy}$$
### Công thức liên hệ giữa tích phân mặt loại II và loại I
- Ta có
$$\iint_S{Pdydz + Qdzdx + Rdxdy} = \iint_S{(P\cos\alpha + Q\cos\beta + R\cos\gamma)dS}$$
- Trong đó, $$(\cos\alpha;\cos\beta\cos\gamma) = \frac{\vec{n}}{|\vec{n}|}$$

### Công thức Ostrogradsky-Gauss (O-G)
- Xét mặt kín $S$, miền bị bao bởi $S$ là $V$, ta có
$$\iint_S{Pdydz + Qdzdx+Rdxdy} = \iiint_V{\bigg(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}\bigg)dxdydz}$$
### Công thức Stokes
- Xét đường cong kín $(C)$ trong không gian, là biên của mặt $S$, ta có
$$\oint_{(C)}{Pdx + Qdy + Rdz} = \iint_S{\bigg(\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z}\bigg)dydz + \bigg(\frac{\partial P}{\partial z} - \frac{\partial R}{\partial x}\bigg)dzdx + \bigg(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\bigg)dxdy}$$
- Chiều của $(C)$ và hướng của $S$ liên hệ với nhau theo _quy tắc bàn tay phải_
