---
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 4
unit: 15
title: Từ trường
---
# Từ trường

>[!definition] Khái niệm
>**Từ trường** là môi trường vật chất đặc biệt bao xung quanh dòng điện

- Khi đặt dòng điện trong từ trường, dòng điện sẽ chịu tác dụng của **[[dinh_luat_ampere|lực từ]]**
- Thông qua từ trường, lực từ được truyền từ dòng điện này đến dòng điện khác với vận tốc hữu hạn

## Vector cảm ứng từ
- **Cảm ứng từ** của từ trường là đại lượng đặc trưng cho từ trường về phương diện tác dụng lực

>[!formula] Định luật Biot-Savard-Laplace
>Xét phần từ dòng điện $Id\vec{l}$ và điểm M cách $Id\vec{l}$ một khoảng $r$. Ta có
>$$d\vec{B} = \frac{\mu\mu_0}{4\pi}\frac{Id\vec{l}\times\vec{r}}{r^3}$$
>Trong đó, $d\vec{B}$:
>- Điểm đặt: M
>- Phương vuông góc với mặt phẳng chứa $Id\vec{l}$ và $\vec{v}$
>- Chiều tuân theo quy tắc tam diện thuận
>- Độ lớn
>$$dB = \frac{\mu\mu_0}{4\pi}\frac{Idl\sin\theta}{r^2}$$ với $\theta$ là góc tạo bởi $Id\vec{l}$ và $\vec{r}$

## Nguyên lí chồng chất từ trường
- Cảm ứng từ tại một điểm bằng tổng vector của các cảm ứng từ thành phần gây ra tại đó
### Với dòng điện hữu hạn
Chia dòng điện thành các phần tử dòng điện $Id\vec{l}$ gây ra cảm ứng từ $d\vec{B}$, ta có
$$B = \int{d\vec{B}} = \int{\frac{\mu\mu_0}{4\pi}\frac{Id\vec{l}\times\vec{r}}{r^3}}$$

### Với tập hợp rời rạc các dòng điện
Giả sử ta có $n$ dòng điện $I_1, I_2,... I_n$, dòng điện $I_k$ gây cảm ứng từ $B_k$, ta có
$$B = \sum_{k=1}^{n}{B_k}$$
## Cường độ từ trường
- Là đại lượng đặc trưng cho khả năng tác dụng lực từ của từ trường, không phụ thuộc vào môi trường
$$\vec{H} = \frac{\vec{B}}{\mu\mu_0}$$
## Cảm ứng từ của một số dòng điện đặc biệt
### Dòng diện thẳng, hữu hạn
- Xét dòng điện $I$ thẳng, hữu hạn và điểm M
![[cam_ung_tu_dong_dien_thang.excalidraw]]
Chia dòng điện thành các phần tử $Id\vec{l}$, gây cảm ứng từ $d\vec{B}$ tại M, ta có
$$d\vec{B} = \frac{\mu\mu_0}{4\pi}\frac{Id\vec{l}\times\vec{r}}{r^3}\,;dB=\frac{\mu\mu_0}{4\pi}\frac{Idl\sin\theta}{r^2}$$
Ta có
$$r = \frac{d}{\sin\theta};\, l= d\cot\theta \Rightarrow dl = \frac{d}{\sin^2\theta}d\theta$$
Vậy ta có
$$dB = \frac{\mu\mu_0}{4\pi}\frac{I}{d}\sin\theta d\theta$$
Vậy cảm ứng từ gây ra do dây thẳng tại điểm M cách dây khoảng $d$
$$B = \int{dB} = \int_{\theta_1}^{\theta_2}{\frac{\mu\mu_0I}{4\pi d}\sin\theta d \theta}$$

>[!formula] Cảm ứng từ do dây dẫn thẳng hữu hạn gây ra
>- Điểm đặt: M
>- Phương: vuông góc với mặt phẳng giữa dây và M
>- Chiều: tuân theo quy tắc tam diện thuận
>- Độ lớn
>$$B = \frac{\mu\mu_0I}{4\pi d}(\cos\theta_1 - \cos\theta_2)$$

Mở rộng, ta có
- Cảm ứng từ do dòng điện thẳng dài vô hạn $B = \frac{\mu\mu_0I}{2\pi d}$
- Cảm ứng từ do nửa dòng điện thẳng, dài vô hạn $B = \frac{\mu\mu_0I}{4\pi d}$
- Cảm ứng từ do dòng điện thẳng gây ra tại điểm nằm trên đường kéo dài của dòng điện $B = 0$

### Dòng điện dạng tròn, M nằm trên trục
- Xét dòng điện có dạng đường tròn tâm $O$, bán kính $R$. Xét điểm $M$ nằm trên trục của đường tròn, cách tâm khoảng $h$
![[cam_ung_tu_duong_tron.excalidraw]]

- Chia dòng điện thành các phần tử dòng điện $Id\vec{l}_1$ và $Id\vec{l}_2$ đối xứng qua O, cảm ứng từ gây ra tại M lần lượt là $d\vec{B}_1$ và $d\vec{B}_2$
- Ta có
$$d\vec{B}_1 = \frac{\mu\mu_0}{4\pi}\frac{Id\vec{l}_1\times\vec{r}}{r^3}$$
$$dB_1 = \frac{\mu\mu_0}{4\pi}\frac{Idl}{r^2}\sin\theta = \frac{\mu\mu_0Idl}{4\pi r^2}$$
Tương tự với $d\vec{B}_2$
Từ đó ta có
$$dB = 2dB_1\cos\alpha = \frac{\mu\mu_0Idl}{2\pi r^2}\frac{R}{r} = \frac{\mu\mu_0IRdl}{2\pi r^3}$$
Lấy tích phân 
$$B = \int_{\text{nửa đường tròn}}{\frac{\mu\mu_0IRdl}{2\pi r^3}} = \frac{\mu\mu_0IR^2}{2r^3}$$

>[!formula] Cảm ứng từ do dòng điện dạng đường tròn gây ra
>$$B = \frac{\mu\mu_0IR^2}{2(R^2+h^2)^{\frac{3}{2}}}$$

Xét moment lưỡng cực từ $\vec{p_m} = I\vec{S}$, trong đó $\vec{S} = S.\vec{n}$, vector pháp tuyến $\vec{n}$ được lấy theo quy tắc bàn tay phải, ta có thể viết lại công thức trên dưới dạng sau:

>[!formula] Cảm ứng từ do dòng điện dạng đường tròn gây ra 
>$$\vec{B} = \frac{\mu\mu_0\vec{p_m}}{2\pi(R^2+h^2)^\frac{3}{2}}$$

>[!formula] Cảm ứng từ tại tâm dòng điện tròn
>$$B = \frac{\mu\mu_0I}{2R}$$

