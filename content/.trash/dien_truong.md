---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 1
unit: 5
title: Điện trường
---

# Điện trường
## Vector cường độ điện trường của điện tích điểm
- **Điện trường** là _dạng vật chất đặc biệt_ xuất hiện trong không gian _xung quanh_ các điện tích.
- Tính chất cơ bản của điện trường: Tác dụng [[dinh_luat_coulomb 1|lực điện]] lên _mọi điện tích_ đặt trong nó. Lực tác dụng này được truyền đi với vận tốc hữu hạn
- Xét điện tích điểm $q$ và điện tích thử $q_0$ có độ lớn rất nhỏ so với $q$, cách $q$ một khoảng $r$. Khi đó $q_0$ chịu tác dụng của lực điện
$$\vec{F}= \frac{qq_0}{4\pi\epsilon\epsilon_0r^2}.\frac{\vec{r}}{r}$$
($\vec{r}$ là vector nối từ $q$ đến $q_0$)
- **Vector cường độ điện trường** là vector:
	- Có điểm đặt tại điểm đặt điện tích thử $q_0$
	- Có phương là đường nối $qq_0$
	- Cùng chiều với $q.\vec{r}$, tức là:
		- Hướng ra nếu $q>0$
		- Hướng vào nếu $q<0$

>[!formula] Độ lớn vector cường độ điện trường do điện tích điểm $q$ gây ra
>$$\vec{E} = \frac{\vec{F}}{q_0}$$
>$$E = \frac{|q|}{4\pi\epsilon\epsilon_0r^2}$$

## Nguyên lí chồng chất điện trường. Điện trường của hệ điện tích

>[!formula] Nguyên lí chồng chất điện trường
>Điện trường tổng hợp tại một điểm bằng tổng vector cường độ điện trường do các thành phần gây ra tại điểm đó

- Đối với hệ điểm phân bố rời rạc $q_1;q_2;...;q_n$, cường độ điện trường tại điểm M:
$$\overrightarrow{E_M} = \sum_{i=1}^{n}{\overrightarrow{E_i}}$$
- Đối với vật rắn tích điện, chia nhỏ vật thành các phần tử vô cùng nhỏ $\mathrm{d}q$, coi như điện tích điểm, $\mathrm{d}q$ gây ra cường độ điện trường $\overrightarrow{\mathrm{d}E}$:
$$\overrightarrow{E_M} = \int_{\text{toàn bộ vật}}{\overrightarrow{\mathrm{d}E}}$$

## Điện trường của một số vật đặc biệt
### Vòng dây kim loại tích điện đều
![[dien_truong_vong_day.excalidraw]]
- Xét dây kim loại tích điện đều uốn thành đường tròn tâm O bán kính $R$, điện tích $q$; điểm H nằm trên trục của vòng dây, cách tâm O một khoảng $h$
- Chia vòng tròn thành cặp đối xứng gồm 2 điện tích điểm $dq_1$ và $dq_2$ đối xứng qua O, ta có
$$dE_1 = dE_2 = \frac{dq}{4\pi\epsilon\epsilon_0r^2}$$
(với $r$ là khoảng cách từ $dq_1$ và $dq_2$ đến H, $r^2 = R^2 + h^2$)
- Phân tích $\overrightarrow{dE_1} = \overrightarrow{dE_{1x}} + \overrightarrow{dE_{1y}}$, trong đó $\overrightarrow{dE_{1x}}$ song song với mặt phẳng chứa đường tròn và $\overrightarrow{dE_{1y}}$ vuông góc với mặt phẳng đó. Chia $\overrightarrow{dE_2}$ tương tự
- Do tính đối xứng nên $\overrightarrow{dE_{1x}}+\overrightarrow{dE_{2x}} = \vec{0}$
- $\overrightarrow{dE_{1y}} = \overrightarrow{dE_{2y}}$
- Xét $\overrightarrow{dE} = \overrightarrow{dE_1} + \overrightarrow{dE_2} = 2\overrightarrow{dE_{1y}}$
- Về độ lớn $dE = 2dE_1\cos\alpha$ với $\alpha$ là góc tạo bởi $HdE_1$ và $OH$
- Từ đó ta có $dE = 2\frac{dq}{4\pi\epsilon\epsilon_0r^2}.\frac{h}{r}$
- Điện trường do cả đường tròn tác dụng lên $H$
$$E = \int_{\text{nửa đường tròn}}{dE} = \int_{\text{nửa đường tròn}}{2\frac{dq}{4\pi\epsilon\epsilon_0r^2}.\frac{h}{r}} = \frac{qh}{4\pi\epsilon\epsilon_0r^3}$$

>[!formula] Điện trường do vòng dây kim loại tích điện đều tác dụng lên điểm trên trục của nó
>- Điểm đặt: M
>- Phương: vuông góc mặt phẳng chứa vòng dây
>- Chiều: $\overrightarrow{OM}$ nếu vòng dây tích điện dương, $\overrightarrow{MO}$ nếu vòng dây tích điện âm
>- Độ lớn
> $$E = \frac{qh}{4\pi\epsilon\epsilon_0(R^2+h^2)^{\frac{3}{2}}}$$

### Thanh thẳng tích điện đều
![[dien_truong_thanh_thang.excalidraw]]
- Xét thanh thẳng đồng chất, tiết diện đều, độ dài $l$, tích điện $q$, mật độ điện dài $\lambda = \frac{q}{l}$
- Xét điểm M nằm trên đường trung trực của thanh, cách thanh khoảng $h$
- Chia thanh thành các đoạn $dl$ cách trung điểm của thanh một khoảng $x$, coi như điện tích điểm mang điện tích $dq$. Ta có $dq = \lambda dl = \frac{q}{l}dl$
- Điện tích $dq$ gây ra tại điểm M điện trường $\overrightarrow{dE}$, ta có $$dE = \frac{dq}{4\pi\epsilon\epsilon_0r^2}$$ với $r = \frac{l^2}{4} + h^2$
- Phân tích $\overrightarrow{dE} = \overrightarrow{dE_x} + \overrightarrow{dE_y}$ trong đó $\overrightarrow{dE_x}$ song song với mặt phẳng khung dây, còn $\overrightarrow{dE_y}$ vuông góc
- Do tính đối xứng của thanh $\int_{\text{toàn bộ thanh}}{\overrightarrow{dE_x}} = \vec{0}$
- Vậy điện trường tổng hợp $\vec{E} = \int_{\text{toàn bộ thanh}}{\overrightarrow{dE}} = \int_{\text{toàn bộ thanh}}{\overrightarrow{dE_y}}$
- Ta có: $dEy = dE\cos\alpha$ với $\alpha$ là góc tạo bởi $OM$ và $Mdl$, $\alpha < 0$ nếu $dl$ nằm bên trái O và $>0$ nếu nằm bên phải
- Ta có
$$E = \int_{\text{toàn bộ thanh}}{dE} =  \int_{\text{toàn bộ thanh}}{dE_y} =  \int_{\text{toàn bộ thanh}}{dE\cos\alpha} =  \int_{\text{toàn bộ thanh}}{\frac{dq}{4\pi\epsilon\epsilon_0r^2}\cos\alpha} =  \int_{\text{toàn bộ thanh}}{\frac{\lambda dl}{4\pi\epsilon\epsilon_0r^2}\cos\alpha}$$
- Ta cũng có
$$x = h\tan\alpha \Rightarrow dl = \frac{h}{\cos^2\alpha}d\alpha = \frac{1}{h}\frac{h^2}{\cos^2\alpha}d\alpha = \frac{r^2}{h}d\alpha$$
Vậy
$$E = \int_{\text{toàn bộ thanh}}{\frac{\lambda d\alpha}{4\pi\epsilon\epsilon_0h}\cos\alpha} = \int_{-\alpha_0}^{\alpha_0}{\frac{\lambda d\alpha}{4\pi\epsilon\epsilon_0h}\cos\alpha} = \frac{\lambda }{4\pi\epsilon\epsilon_0h}.2.\sin\alpha_0 = \frac{\lambda }{2\pi\epsilon\epsilon_0h}.\frac{\frac{l}{2}}{\sqrt{\frac{l^2}{4} + h^2}} = \frac{q}{4\pi\epsilon\epsilon h. \sqrt{\frac{l^2}{4} + h^2}}$$

>[!formula] Điện trường do thanh thẳng đồng chất tiết diện đều tác dụng lên điểm trên đường trung trực của nó
>- Điểm đặt: M
>- Phương: đường trung trực
>- Chiều: $\overrightarrow{OM}$ nếu $q>0$, $\overrightarrow{MO}$ nếu $q<0$
>- Độ lớn
>$$E = \frac{q}{4\pi\epsilon\epsilon_0 h \sqrt{\frac{l^2}{4} + h^2}}$$

### Đĩa tròn tích điện đều
- Xét đĩa tròn tâm $O$ bán kính $R$ tích điện đều với mật độ điện mặt là $\sigma$
- Điểm $M$ nằm trên trục của đĩa, cách tâm $O$ một khoảng bằng $h$
- Chia đĩa thành các hình xuyến tạo từ vòng dây bán kính $r$ và vòng dây bán kính $r + dr$ có điện tích $dq$. Ta có $dq = 2\pi\sigma r dr$
- Điện trường do vòng dây gây ra tại $M$ là
$$dE = \frac{dq.h}{4\pi\epsilon\epsilon_0(r^2+h^2)^{\frac{3}{2}}} = \frac{2\pi\sigma rh dr}{4\pi\epsilon\epsilon_0(r^2+h^2)^{\frac{3}{2}}}$$
- Vậy điện trường do đĩa tròn gây ra tại M
$$E = \int_{\text{toàn bộ đĩa}}{dE} = \int_0^R{\frac{2\pi\sigma rh dr}{4\pi\epsilon\epsilon_0(r^2+h^2)^{\frac{3}{2}}}} = \frac{\sigma h}{4\epsilon\epsilon_0}\int_0^R{\frac{2r}{(r^2+h^2)^{\frac{3}{2}}}} = \frac{\sigma h}{2\epsilon\epsilon_0}\bigg(\frac{1}{h} - \frac{1}{\sqrt{R^2+h^2}}\bigg) = \frac{\sigma}{2\epsilon\epsilon_0}\bigg(1-\bigg(1+\frac{R^2}{h^2}\bigg)^{-\frac{1}{2}}\bigg)$$
- Khi cho $R \rightarrow +\infty$, ta có điện trường của mặt phẳng vô hạn tích điện đều gây ra tại điểm M cách mặt phẳng khoảng $h$ là
$$E = \frac{\sigma}{2\epsilon\epsilon_0}$$

>[!formula] Điện trường do đĩa tròn tích điện đều gây ra cho điểm M nằm trên trục đĩa
>- Điểm đặt: M
>- Phương: vuông góc với đĩa
>- Chiều: $\overrightarrow{OM}$ nếu $q>0$, $\overrightarrow{MO}$ nếu $q<0$
>- Độ lớn:
> $$E = \frac{\sigma}{2\epsilon\epsilon_0}\bigg(1-\bigg(1+\frac{R^2}{h^2}\bigg)^{-\frac{1}{2}}\bigg)$$


>[!formula] Điện trường do mặt phẳng vô hạn tích điện đều gây nên
>- Điểm đặt: M
>- Phương: trùng phương với vector pháp tuyến của mặt phẳng
>- Chiều: ra xa mặt phẳng nếu tích điện dương, đi vào mặt phẳng nếu tích điện âm
>- Độ lớn
>$$E = \frac{\sigma}{2\epsilon\epsilon_0}$$
>- Là **điện trường đều**
## Đường sức điện
- **Đường sức điện trường** là những đường cong mà tiếp tuyến tại một điểm là vector cường độ điện trường tại điểm đó. Chiều của đường sức điện là chiều của vector cường độ điện trường.
- Tập hợp các đường sức điện được gọi là **điện phổ**
- Tính chất:
	- cong, hở, từ dương sang âm
	- không giao nhau
	- biểu diễn hình ảnh điện trường: thưa -> yếu, mau -> mạnh, đều -> đều