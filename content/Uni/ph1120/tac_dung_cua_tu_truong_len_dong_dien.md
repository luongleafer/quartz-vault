---
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 4
unit: 17
title: Tác dụng của từ trường lên dòng điện
---
# Tác dụng của từ trường lên dòng điện
Xét dòng điện có cường độ $I$, đặt trong [[tu_truong|từ trường]] đều $\vec{B}$, lực do $\vec{B}$ tác dụng lên một phần tử dòng điện $Id\vec{l}$:

$$d\vec{F} = Id\vec{l} \times \vec{B}$$
Ta có: $d\vec{F}$:
- Điểm đặt: $Id\vec{l}$
- Phương: vuông góc với mặt phẳng chứa $Id\vec{l}$ và $\vec{B}$
- Chiều: tuân theo quy tắc tam diện thuận
- Độ lơn $dF = BIdl\sin\theta$ với $\theta$ là góc giữa $\vec{B}$ và $Id\vec{l}$

## Lực tương tác giữa hai dòng điện thẳng song song dài vô hạn
- Xét hai dây điện có cường độ lần lượt là $I_1$ và $I_2$, đặt song song nhau, cách nhau khoảng $d$.
![[tuong_tac_tu_hai_dong_dien.excalidraw]]
- Do $I_1d\vec{l_1}$ và $\vec{B}_2$ vuông góc nên ta có $dF = BIdl$
- Vậy lực do [[tu_truong#Vector cảm ứng từ|cảm ứng từ]] của dây điện thứ hai tác dụng lên dây thứ nhất
$$F_{21} = \int_{\text{dây 1}}{BIdl} = B_2I_1l_1 = \frac{\mu\mu_0I_1I_2l}{2\pi d}$$
Tương tự ta có $F_{12} = F_{21}$

>[!formula] Lực tương tác giữa hai dòng điện thẳng song song
>$$F = \frac{\mu\mu_0I_1I_2l}{2\pi d}$$

Từ đó ta có
>[!definition] Định nghĩa đơn vị Ampere (A)
>1 Ampere (A) là cường độ dòng điện chạy qua hai dây dẫn thẳng, vô hạn, song song, cách nhau khoảng cách 1m trong chân không sao cho lực tác dụng lên 1m chiều dài dây có độ lớn $2\times 10^{-7} N$

## Lực từ tác dụng lên mạch kín
- Xét khung dây có dạng hình chữ nhật $ABCD$, kích thước $a \times b$. Khung dây có thể chuyển động quay quanh trục $\Delta$ song song với các cạnh độ dài $a$
- Đặt khung trong từ trường đều có vector cảm ứng từ $\vec{B}$ vuông góc với trục quay, ban đầu tạo với vector pháp tuyến của khung dây một góc $\theta$
![[tu_truong_khung_day.excalidraw]]
- Khi đặt khung dây trong từ trường, CB và AD chịu tác dụng của $\vec{F_2}$ và $\vec{F_4}$ nhưng $\vec{F_2}+\vec{F_4} =\vec{0}$
- BA và DC chịu tác dụng của $\vec{F_1}$ và $\vec{F_3}$ gây chuyển động quay quanh trục $\Delta$
- Moment cặp ngẫu lực $\vec{F_1}$ và $\vec{F_3}$:
$$\mu = 2F_1\frac{b}{2}\sin\theta=F_1b\sin\theta = IaBb\sin\theta = ISB\sin\theta = p_m B\sin\theta$$
Từ đó ta có
>[!formula] Moment ngẫu lực từ
>$$\vec{\mu} = \vec{p_m} \times \vec{B}$$

- Dưới tác dụng của cặp ngẫu lực, khung nhận một công
$$d\vec{A} = \vec{\mu}d\theta; dA = \mu d \theta$$
- Khi cho khung chuyển động từ góc $\theta$ về $0$ ta có
$$A = -\int_{\theta}^{0}{dA} = -\int_{\theta}^{0}{p_mB\sin\theta d \theta} = p_mB(1-\cos\theta)$$
- Do công của từ trường bằng độ giảm thế năng của khung dây trong từ trường, nên ta có thể viết
$$A = W_t(\theta) - W_t(0)$$
Từ đó ta có
>[!formula] Thế năng của khung dây trong từ trường
>$$W_t = - \vec{p_m}\cdot\vec{B}$$

## Công của lực từ

>[!formula] Công của lực từ
>$$A = I(\phi_2 - \phi_1)$$


