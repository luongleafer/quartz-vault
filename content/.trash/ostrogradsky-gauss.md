---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 1
unit: 6
title: Điện cảm, Điện thông. Định lý Ostrogradsky-Gauss (OG)
---

# Định lý Ostrogradsky-Gauss (OG)
## Vector điện cảm
- là đại lượng vector đặc trưng cho tính chất của [[dien_truong 1|điện trường]] _không phụ thuộc vào môi trường_
>[!formula] Vector điện cảm
>$$\overrightarrow{D} = \overrightarrow{E}\epsilon\epsilon_0$$

- Tính chất: _liên tục_ khi qua mặt phân cách giữa các môi trường có hằng số điện môi khác nhau.

## Điện thông
- là đại lượng vô hướng biểu thị số đường sức điện gửi qua một mặt $S$
- Để xác định điện thông gửi qua mặt $S$, ta chia $S$ thành các mảnh $\mathrm{d}S$ vô cùng nhỏ, trên các mảnh này từ trường là từ trường đều.
- Ta có vi phân điện thông $\mathrm{d}\phi = \overrightarrow{D}.\overrightarrow{\mathrm{d}S} = D.\mathrm{d}S.\cos{\alpha}$ với $\alpha$ là góc giữa $\overrightarrow{D}$ và vector pháp tuyến của $\mathrm{d}S$
- Khi đó, điện thông gửi qua mặt S: $\phi = \int_{S}{\mathrm{d}\phi} = \int_{S}{\overrightarrow{D}.\overrightarrow{\mathrm{d}S}}$
>[!formula] Định lý Ostrogradsky-Gauss
>Điện thông gửi qua một mặt kín bằng tổng đại số của các điện tích nằm trong mặt kín đó
>$$\phi = \sum{q}$$

## Ứng dụng định lí OG để tìm cường độ điện trường
### Mặt cầu tích điện đều
- Xét mặt cầu tâm O bán kính $R$ rỗng, tích điện đều và có điện tích $q$.
- Điểm M cách tâm $O$ khoảng cách $r$
- Xét trường hợp $r \ge R$.
- Dựng mặt Gauss là mặt cầu tâm O đi qua M. Tại mọi điểm trên mặt Gauss, D là hằng số, $\vec{D}$ và $\vec{n}$ cùng phương, cùng chiều nên ta có
$$\phi = \int_{S}{\overrightarrow{D}.\overrightarrow{\mathrm{d}S}} = \int_S{D.\mathrm{d}S} = DS = D.4\pi r^2$$
- Theo định lí OG, ta có 
$$\phi = \sum{q} = q$$
Vậy $$D.4\pi r^2 = q \Leftrightarrow D = \frac{q}{4\pi r^2} \Leftrightarrow E = \frac{q}{4\pi\epsilon\epsilon_0r^2}$$
- Xét trường hợp $r < R$, do không có điện tích trong mặt Gauss, $\phi = 0 \Leftrightarrow D = E = 0$
>[!formula] Điện trường do mặt cầu tích điện đều gây ra tại điểm M
>$$E = \begin{cases}0 \text {     nếu     } r < R \\ \frac{q}{4\pi\epsilon\epsilon_0r^2} \text{     nếu     } r \ge R\end{cases}$$

### Mặt phẳng vô hạn tích điện đều
- Xét mặt phẳng vô hạn tích điện đều, mật độ điện mặt là $\sigma$
- Điểm M cách mặt phẳng khoảng cách $h$
- Lấy M' đối xứng với M qua mặt phẳng H.
- Dựng mặt Gauss là mặt trụ có hai đáy $(M;r)$ và $(M';r)$, đường sinh vuông góc với mặt phẳng
- Xét điện thông gửi qua mặt trụ Gauss
$$\phi = \oint_{\text{trụ}}{\overrightarrow{D}\,\overrightarrow{dS}} = \oint_{S_1}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{S_2}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{S_{xq}}{\overrightarrow{D}\,\overrightarrow{dS}}$$
($S1$, $S2$ là hai đáy của trụ, $S_{xq}$ là mặt xung quanh của trụ)
- Nhận xét: Trên $S_{xq}$, vector pháp tuyến $\vec{n}$ luôn vuông góc với $\vec{D}$ nên $\overrightarrow{D}\,\overrightarrow{dS} = 0$ 
- Trên $S_1$ và $S_2$, $\overrightarrow{n}$ và $\overrightarrow{D}$ luôn cùng phương, cùng chiều
$$\phi = 2\oint_{S_1}{D.dS} = 2DS$$
- Theo định lí OG ta có
$$\phi = \sum{q} = \sigma.S$$
- Vậy 
$$2DS = \sigma S \Leftrightarrow D = \frac{\sigma}{2} \Leftrightarrow E = \frac{\sigma}{2\epsilon\epsilon_0}$$
- Kết quả này phù hợp với công thức thu được từ [[dien_truong 1#Nguyên lí chồng chất điện trường. Điện trường của hệ điện tích|Nguyên lí chồng chất điện trường]]

### Sợi dây dài vô hạn tích điện đều
- Xét sợi dây dài vô hạn, tích điện đều với mật độ điện mặt $\lambda$
- Điểm M cách sợi dây một khoảng $r$
- Dựng mặt Gauss là mặt trụ, có trục là sợi dây, đường sinh song song với sợi dây, hai đáy vuông góc sợi dây, bán kính $r$, độ dài đường sinh là $l$
- Điện thông gửi qua mặt Gauss:
$$\phi = \oint_S{\overrightarrow{D}\,\overrightarrow{dS}} = \oint_{S_1}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{S_2}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{S_{xq}}{\overrightarrow{D}\,\overrightarrow{dS}}$$
- Trong đó:
	- $S_1$ và $S_2$ là hai đáy của trụ. Trên hai mặt này, $\overrightarrow{D}$ luôn vuông góc với $\overrightarrow{n}$ nên $\overrightarrow{D}.\overrightarrow{dS} = 0$
	- $S_{xq}$ là mặt bên của trụ, trên mặt này, $\overrightarrow{D}$ và $\overrightarrow{n}$ luôn cùng phương, cùng chiều
- Từ đó ta có:
$$\phi = \oint_{S_{xq}}{\overrightarrow{D}\,\overrightarrow{dS}} = \oint_{S_{xq}}{D.dS} = D.S_{xq} = D.2\pi r l$$
- Theo định lí OG ta có
$$\phi = \sum q = \lambda.l$$
Vậy từ đó
$$\lambda.l = D.2\pi r l\Leftrightarrow D = \frac{\lambda}{2\pi r}\Leftrightarrow E = \frac{\lambda}{2\pi\epsilon\epsilon_0 r}$$
>[!formula] Điện trường do sợi dây dài vô hạn tích điện đều gây ra
>- Điểm đặt: M
>- Phương: vuông góc với sợi dây
>- Chiều: ra khỏi sợi dây nếu $\lambda > 0$, đi vào sợi dây nếu $\lambda < 0$
>- Độ lớn
>$$E = \frac{\lambda}{2\pi\epsilon\epsilon_0 r}$$