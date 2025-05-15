---
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 1
unit: 7
title: Điện thế
---

# Điện thế
## Công của lực tĩnh điện
- Xét điện tích điểm $q$ và điện tích thử $q_0$ có độ lớn rất nhỏ so với $q$
- Lực điện làm $q_0$ di chuyển theo đường cong $(C)$ từ điểm (1) đến điểm (2) lần lượt cách $q$ một khoảng là $r_1$ và $r_2$
- Chia đường cong $(C)$ thành các đoạn vô cùng nhỏ $\overrightarrow{\mathrm{d}s}$, coi như đường thẳng và ở đó điện trường đều.
- Công vi phân $\mathrm{d}A = \overrightarrow{F}.\overrightarrow{\mathrm{d}s} = F\mathrm{d}s\cos\alpha=F\mathrm{d}r$
- Như vậy, công do lực điện gây ra khi di chuyển $q_0$ từ điểm (1) đến điểm (2) là:
$$A = \int_{(C)}{dA} = \int_{r_1}^{r_2}{F\mathrm{d}r} = \int_{r_1}^{r_2}{\frac{q_0.q}{4\pi\epsilon\epsilon_0r^2}\mathrm{d}r} = \frac{q.q_0}{4\pi\epsilon\epsilon_0}(\frac{1}{r_1} - \frac{1}{r_2})$$
- Như vậy, công của lực điện khi dịch chuyển điện tích _không phụ thuộc vào đường đi_, chỉ phụ thuộc vào _vị trí_ điểm đầu và điểm cuối.

## Trường tĩnh điện
- Trường tĩnh điện là một **trường thế**, vì công của lực điện khi dịch chuyển điện tích theo một chu trình kín bằng 0
$$\oint_{(C)}{\mathrm{d}A} = 0$$



>[!formula] Thế năng của điện tích trong trường tĩnh điện
>$$W_t = \frac{q.q_0}{4\pi\epsilon\epsilon_0r}$$

^thenang



## Điện thế
- Là đại lượng đặc trưng cho điện trường
$$V = \frac{W_t}{q_0}$$
- Đối với điện tích điểm $V = \frac{q}{4\pi\epsilon\epsilon_0r}$
- Đối với hệ điện tích điểm $V = \sum{V_i}$
- Đối với vật rắn tích điện $V = \int_{\text{toàn bộ vật}}{dV}$
- Đối với điện trường bất kì $V = \int_M^\infty{\overrightarrow{E}.\overrightarrow{\mathrm{d}s}}$
- Như vậy, điện thế của một điểm trong điện trường là đại lượng có trị số bằng công của lực tĩnh điện di chuyển điện tích +1C từ điểm đó ra xa vô cùng

## Hiệu điện thế
- Là đại lượng bằng công của lực điện di chuyển điện tích +1C giữa hai điểm đó
$$U_{12} = \int_{(1)}^{(2)}{\frac{dA}{q_0}} = \frac{A_{12}}{q_0} = \int_{(1)}^{(2)}\overrightarrow{E}.\overrightarrow{ds}$$
## Mặt đẳng thế
- là quỹ tích các điểm có cùng điện thế
- Đặc điểm:
	- các mặt đẳng thế không bao giờ cắt nhau
	- cong di chuyển điện tích trên mặt đẳng thế = 0
	- $\overrightarrow{E}$ trên mặt đẳng thế luôn vuông góc với mặt đẳng thế đó
## Mối liên hệ giữa điện trường và điện thế
- Xét công dịch chuyển điện tích $q_0$ đi từ điện thế $V$ đến điện thế $V+dV$ ($dV > 0$)
- Ta có $dA = \overrightarrow{E}\,\overrightarrow{ds} = q_0\overrightarrow{E}\,\overrightarrow{ds}$
- Lại có $dA = q_0[V-(V+dv)] = -q_0dV$
- Từ đó ta có $\overrightarrow{E}\,\overrightarrow{ds} = -dV = Eds\cos\alpha$
- Do $\cos\alpha < 0$ nên $\alpha$ là góc tù

>[!note] Nhận xét
>Điện trường luôn đi theo chiều giảm điện thế

- Đặt $E_s$ là hình chiếu của $E$ lên $ds$ ta có

>[!formula] Mối liên hệ giữa cường độ điện trường và điện thế
>$$E_s = \frac{-dV}{ds}$$
>$$E =  -\overrightarrow{\nabla V}$$


## Hiệu điện thế trong điện trường giữa các vật tích điện

### HĐT giữa hai mặt phẳng vô hạn tích điện đều, trái dấu, cách nhau khoảng d

- Ta có $$E_s = E = \frac{\sigma}{\epsilon\epsilon_0}$$
- Vậy
$$U = \int_{(1)}^{(2)}{E_s\,ds} = \int_0^d{\frac{\sigma}{\epsilon\epsilon_0}ds} = \frac{\sigma d}{\epsilon \epsilon_0}$$

>[!formula] HĐT giữa hai mặt phẳng vô hạn tích điện đều, trái dấu
>$$U = \frac{\sigma d}{\epsilon \epsilon_0}$$

### HĐT giữa hai điểm nằm trong điện trường của mặt cầu tích điện đều
- Hai điểm lần lượt cách tâm khoảng cách $r_1$ và $r_2$
- Xét sự dịch chuyển từ $(1)$ đến $(2)$ theo phương bán kính $\overrightarrow{r}$
- Do $\overrightarrow{E}$ cùng phương, cùng chiều với $\overrightarrow{r}$ tại mọi điểm nên $$E_r = E = \frac{q}{4\pi\epsilon\epsilon_0 r^2}$$
- Từ đó ta có
$$U_{12} = \int_{r_1}^{r_2}{E_r\,dr} = \int_{r_1}^{r_2}{\frac{q}{4\pi\epsilon\epsilon_0 r^2}} = \frac{q}{4\pi\epsilon\epsilon_0}\bigg(\frac{1}{r_1} - \frac{1}{r_2}\bigg)$$
>[!formula] HĐT giữa hai điểm nằm trong điện trường của mặt cầu tích điện đều
>$$U_{12} = \frac{q}{4\pi\epsilon\epsilon_0}\bigg(\frac{1}{r_1} - \frac{1}{r_2}\bigg)$$

Tương tự ta có các kết quả sau

### HĐT giữa hai điểm nằm trong điện trường của mặt trụ tích điện đều

>[!formula] HĐT giữa hai điểm nằm trong điện trường của mặt trụ
>- Khoảng cách từ hai điểm tới trục của trụ lần lượt là $r_1$ và $r_2$, ta có
>$$U_{12} = \frac{\lambda}{2\pi\epsilon\epsilon_0}\ln\bigg(\frac{r_2}{r_1}\bigg)= \frac{\sigma R}{\epsilon\epsilon_0}\ln\bigg(\frac{r_2}{r_1}\bigg)$$