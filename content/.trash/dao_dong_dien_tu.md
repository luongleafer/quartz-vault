---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 7
unit: 25
title: Dao động điện từ
---

## Dao động
>[!definition] Khái niệm
>**Dao động** là các chuyển động có tọa độ biến thiên lặp lại theo thời gian, được mô tả dưới hàm sin/cos

Ví dụ, một vật có tọa độ được biểu diễn bởi hàm $x(t) = A\cos(\omega t + \varphi)$ là một dao động
Các đại lượng:
- Biên độ $A$: đặc trưng cho phạm vi dao động
- Chu kì $T$: khoảng thời gian lặp lại của dao động
- Tần số $f$: số chu kì thực hiện trong một đơn vị thời gian
- Góc pha $\varphi$: xác định trạng thái ở thời điểm ban đầu $t = 0$

### Các dạng dao động
- Dao động **điều hòa**:
	- không có sự cản trở của các yếu tố bên ngoài nư ma sát
	- biên độ không đổi theo thời gian
	- năng lượng luôn được bảo toàn
- Dao động **tắt dần**
	- có biên độ giảm dần theo thời gian
	- năng lượng bị tiêu hao theo thời gian
- Dao động **cưỡng bức**
	- có sự cản trở của yếu tố bên ngoài
	- chịu tác dụng của lực kích thích bên ngoài
	- có sự cộng hưởng giữa năng lượng tác động bên ngoài và năng lượng tiêu hao bên trong

## Dao động điện từ
### Dao động điện từ điều hòa trong mạch LC
- Xét mạch gồm:
	- cuộn cảm $L$
	- tụ điện $C$
	- nguồn điện
! cần hình ảnh .-.
- Khi K ở vị trí (1), nguồn nạp cho tụ điện lượng điện tích $Q_0 = C.U_0$
- Khi K chuyển sang vị trí (2), tụ phóng điện qua cuộn cảm, làm xuất hiện [[hien_tuong_tu_cam|dòng điện tự cảm]] $I_{tc}$ cùng chiều với dòng điện mạch ngoài $I$, tham gia vào quá trình nạp lại cho tụ điện
- Năng lượng điện trường được chuyển hóa thành năng lượng từ trường và ngược lại làm cho dao động tuần hoàn theo thời gian
- Xét năng lượng toàn phần
$$\frac{q^2}{2C} + \frac{1}{2}Li^2 = \mathrm{const}$$
- Lấy đạo hàm theo thời gian
$$\frac{q}{C}\frac{\mathrm{d}q}{\mathrm{d}t}+Li\frac{\mathrm{d}i}{\mathrm{d}t} = 0$$
- Do $i = \frac{\mathrm{d}q}{\mathrm{d}t}$ nên ta có
$$i\frac{q}{C} + iL\frac{\mathrm{d^2q}}{\mathrm{d}t^2} = 0$$
- Thu gọn $i$
$$\frac{q}{C}+L\frac{d^2q}{\mathrm{d}t^2} = 0$$
- Chia cả hai vế cho $L \neq 0$
$$\frac{q}{LC}+\frac{\mathrm{d}^2q}{\mathrm{d}t^2} = 0 (*)$$
Giải $(*)$ cho ta phương trình của q
$$q = q_0\cos(\omega_0t+\varphi)$$
với $$\omega_0 = \frac{1}{\sqrt{LC}}$$
Ngoài ra ta có
$$i = \frac{\mathrm{d}q}{\mathrm{d}t} = -q_0\omega_0\sin(\omega_0t+\varphi)$$
- Năng lượng điện từ
$$W = W_e{max} = W_m{max} = \frac{q_0^2}{2C} = \frac{1}{2}Li_0^2$$
### Dao động điện từ tắt dần trong mạch RLC
- Xét mạch điện gồm:
	- cuộn cảm $L$
	- tụ điện $C$
	- điện trở $R$
	- nguồn điện
- Trên điện trở $R$ xảy ra [hiệu ứng tỏa nhiệt Joule-Lenz](https://en.wikipedia.org/wiki/Joule_heating), khiến năng lượng điện từ tiêu hao.
- Trong khoảng thời gian $\mathrm{d}t$, năng lượng mất đi do tỏa nhiệt là
$$-\mathrm{d}W = RI^2\mathrm{d}t$$
- Do $W = \frac{q^2}{2C} + \frac{1}{2}LI^2$ nên ta có
$$\frac{\mathrm{d}W}{\mathrm{d}t} = \frac{q}{C}\frac{\mathrm{d}q}{\mathrm{d}t} + LI\frac{\mathrm{d}I}{\mathrm{d}t} = -RI^2$$
- Thay $\frac{\mathrm{d}q}{\mathrm{d}t} = I$ và rút gọn $I$, ta có
$$\frac{q}{C}+L\frac{\mathrm{d}I}{\mathrm{d}t} = -RI$$
hay
$$\frac{q}{LC} + \frac{\mathrm{d}I}{\mathrm{d}t}+ \frac{IR}{L} = 0$$
$$\Leftrightarrow \frac{1}{LC}q + \frac{R}{L}\frac{\mathrm{d}q}{\mathrm{d}t} + \frac{\mathrm{d}^2q}{\mathrm{d}t^2}(**)$$
Đặt $\beta = \frac{R}{2L}$, $\omega_0 = \frac{1}{\sqrt{LC}}$, nghiệm của phương trình $(**)$ có dạng
$$q = q_0e^{-\beta t}\cos(\omega t+ \varphi)$$
- Trong đó $$\omega = \sqrt{\omega_0^2 - \beta^2}$$
- Như vậy $q$ dao động tắt dần do có biên độ giảm dần theo thời gian 
- $\beta$ được gọi  là **hệ số tắt dần**
- Dao động chỉ xuất hiện khi $$\frac{1}{LC}>\frac{R^2}{4L^2} \Leftrightarrow R < 2\sqrt{\frac{L}{C}}$$
### Dao động cưỡng bức
- Xét mạch RLC được nối với nguồn điện xoay chiều $\epsilon(t) = \epsilon_0\sin(\Omega t)$ có tác dụng duy trì dao động.
- Trong thời gian $\mathrm{d}t$, nguồn $\epsilon$ cung cấp cho mạch  một năng lượng có giá trị $\epsilon I \mathrm{d}t$
Ta có
$$\epsilon I\mathrm{d}t = \mathrm{d}W + RI^2\mathrm{d}t$$
$$\epsilon I = RI^2 + \frac{\mathrm{d}W}{\mathrm{d}t}$$
$$\epsilon I = \frac{qI}{C} + LI\frac{\mathrm{d}I}{\mathrm{d}t} + RI^2$$
$$\epsilon = \epsilon_0\sin(\Omega t) = \frac{q}{C} + L\frac{dI}{dt} + RI$$
Lấy đạo hàm theo thời gian
$$\epsilon_0\Omega\cos(\Omega t) = \frac{I}{C} + L\frac{\mathrm{d}^2I}{\mathrm{d}t^2} + 2R \frac{\mathrm{d}I}{\mathrm{d}t}$$
Nghiệm của phương trình trên có dạng
$$I = I_0\cos(\Omega t + \varphi)$$
với
$$I_0 = \frac{\epsilon_0}{Z}$$$$Z^2 = R^2 + (Z_L - Z_C)^2; Z_L = \Omega L , Z_C = \frac{1}{\Omega C}$$
- Khi $Z_L = Z_C$, hay $\Omega = \frac{1}{\sqrt{LC}}$, $I_0$ là lớn nhất, hiện tượng này được gọi là **cộng hưởng điện**

