---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 5
unit: 21
title: Hiện tượng tự cảm
---
>[!definition] Định nghĩa
>Là hiện tượng xảy ra trong mạch kín, khi cường độ dòng điện trong mạch biến đổi khiến cho từ thông gửi qua mạch biến đổi, làm xuất hiện dòng điện cảm ứng

## Độ tự cảm
>[!definition] Độ tự cảm
>- là đại lượng vật lí đặc trưng cho khả năng chống lại sự biến đổi của dòng điện trong mạch
>- thể hiện tính quán tính của mạch kín

- Độ tự cảm được kí hiệu là $L$, đơn vị $H$
- [[tu_thong_dinh_luat_gauss|Từ thông]] gửi qua mạch kín 
$$\phi = LI \Leftrightarrow L = \frac{\phi}{I}$$
- Xét ống dây chiều dài $l$ được cuốn bởi $N$ vòng dây sít nhau và dòng điện cường độ $I$ chạy qua
- Ta có 
$$\phi = N\vec{B}\cdot\vec{S}=NBS = N\mu\mu_0\frac{NI}{l}S$$
$$\Leftrightarrow L = \frac{\phi}{I} = \frac{\mu\mu_0N^2S}{l}$$

>[!formula] Độ tự cảm của ống dây
>$$L = \frac{\mu\mu_0N^2S}{l}$$

## Hiệu ứng bề mặt
- Khi có dòng điện cao tần chạy qua một dây dẫn, dòng điện hầu như chỉ chạy trên bề mặt của dây dẫn
- Giải thích: Xét dòng điện cao tần chạy qua ống trụ
	- Khi $I$ tăng: trong lòng dây dẫn sinh ra $I_{tc}$ có từ trường chống lại sự biến thiên tăng của từ thông:
		- Trên bề mặt: $I \uparrow\uparrow I_{tc}$
		- Trong lòng ống dây $I \uparrow \downarrow I_{tc}$
	- Khi $I$ giảm: dòng điện cảm ứng đổi chiều, dòng điện trên bề mặt giảm nhiều hơn trong lòng ống dây
	- Đối với dòng điện cao tần, dòng tự cảm tác dụng mạnh ở phần lõi, gần như bị triệt tiêu nên chỉ chạy trên lớp bề mặt của dây
- Ứng dụng
	- Sử dụng ống rỗng để dẫn dòng cao tần
	- Tôi vật liệu kim loại bằng dòng cao tần
## Năng lượng từ trường

### Năng lượng từ trường của ống dây
- Xét mạch điện như hình vẽ (cần hình vẽ)
- Khi khóa K đóng, dòng điện ổn định với cường độ $I_0$
- Xét quá trình đóng/mở khóa K với khoảng thời gian vô cùng nhỏ $\Delta t$
	- Khi đóng K, $I$ tăng đến giá trị $I_0$. Khi đó $I_{tc} \uparrow \downarrow I_0$ và $I = I_0 - I_{tc} < I_0$
	- Khi mở K, $I$ giảm, $I_{tc}\uparrow \uparrow I_0$, $I = I_0+I_{tc} > I_0$
- Như vậy trong quá trình đóng/mở mạch, một dạng năng lượng được tích lũy trong mạch từ của ống dây được chuyển hóa thành năng lượng mạch ngoài
$$\begin{array}{l}
&\epsilon+\epsilon_{tc} = Ri \\
\Rightarrow & \epsilon - L\frac{\mathrm{d}i}{\mathrm{d}t} = Ri \\
\Rightarrow & \epsilon = Ri + L\frac{\mathrm{d}i}{\mathrm{d}t} \\
\Rightarrow & \epsilon i \mathrm{d}t = Ri^2 \mathrm{d}t + Li\mathrm{d}i\\
\end{array}
$$

- $\epsilon i \mathrm{d}t$ là năng lượng mạch ngoài, $Ri^2\mathrm{d}t$ là nhiệt lượng Joule-Lenz tỏa ra trên điện trở, vậy năng lượng từ trường
$$dW_m = Li\mathrm{d}i$$
- Xét năng lượng từ trường khi $i$ tăng từ $0$ đến $I$
$$W_m = \int_{0}^{I}{Li\mathrm{d}i} = \frac{1}{2}LI^2$$

>[!formula] Năng lượng từ trường của ống dây
>$$W_m = \frac{1}{2}LI^2$$

- Xét năng lượng từ trường trên một đơn vị thể tích (mật độ năng lượng từ trường)
$$
\begin{array}{ll}
\omega_m &= \frac{W_m}{V} \\
&= \frac{LI^2}{2Sl} \\
&= \frac{\frac{\mu\mu_0n^2S}{l}I^2}{2Sl} \\
&= \frac{1}{2}\frac{\mu\mu_0n^2I^2}{l^2} \\
&= \frac{1}{2}\frac{\mu\mu_0nI}{l}\frac{nI}{l} \\
&= \frac{1}{2}BH
\end{array}
$$

>[!formula] Mật độ năng lượng từ trường
>$$\omega_m = \frac{1}{2}BH$$

- Xét điện trường bất kì có cảm ứng từ $B$ và cường độ $H$ trong không gian $V$, chia từ trường thành các khối $\mathrm{d}V$ vô cùng nhỏ, trong mỗi khối có từ trường đều, khi đó:

>[!formula] Năng lượng của từ trường bất kì
>$$W_m = \frac{1}{2}\iiint_V{BHdV}$$

