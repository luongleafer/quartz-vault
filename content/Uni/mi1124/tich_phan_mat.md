---
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 5
unit: 9
title: Tích phân mặt
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
