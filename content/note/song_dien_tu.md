---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 7
unit: 26
title: Sóng điện từ
---
# Sóng điện từ
>[!definion] Khái niệm
>**Sóng điện từ** là sự lan truyền của [[truong_dien_tu|điện từ trường]] biên thiên trong không gian

## Phương trình sóng điện từ
- Ta có hệ phương trình Maxwell trong chân không:
$$\begin{array}{ll}
\overrightarrow{\mathrm{rot}}\vec{E} = -\frac{\partial\vec{B}}{\partial t}(1)&&\overrightarrow{\mathrm{rot}}\vec{H} = \frac{\partial\vec{D}}{\partial t} \\
\mathrm{div}\vec{D} = 0 && \mathrm{div}\vec{B}=0
\end{array}$$
- Lấy rot hai vế của $(1)$, ta có
$$\overrightarrow{\mathrm{rot}}(\overrightarrow{\mathrm{rot}}(\vec{E})) = - \overrightarrow{\mathrm{rot}}(\frac{\partial \vec{B}}{\partial t})
$$
$$\Leftrightarrow \overrightarrow{\mathrm{grad}}(\mathrm{div}\vec{E}) - \vec{\nabla}^2\vec{E} = -\frac{\partial}{\partial t}(\overrightarrow{\mathrm{rot}}\vec{B})$$
$$\Leftrightarrow -\vec{\nabla}^2\vec{E} = -\mu_0\frac{\partial}{\partial t}(\overrightarrow{\mathrm{rot}}\vec{H}) = -\mu_0\frac{\partial^2\vec{D}}{\partial t^2} = -\mu_0\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2}$$
Vậy ta có
$$\vec{\nabla}^2\vec{E}-\mu_0\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2} =0$$
Tương tự
$$\vec{\nabla}^2\vec{B}-\mu_0\epsilon_0\frac{\partial^2\vec{B}}{\partial t^2} = 0$$
- Đây là phương trình truyền điện trường và từ trường trong chân không với vận tốc $\frac{1}{\sqrt{\mu_0\epsilon_0}} = c$ là vận tốc ánh sáng.
- Đối với môi trường khác, ta có
$$\begin{array}{l}
\vec{\nabla}^2\vec{E}-\mu\mu_0\epsilon\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2} =0 \\
\vec{\nabla}^2\vec{B}-\mu\mu_0\epsilon\epsilon_0\frac{\partial^2\vec{B}}{\partial t^2} = 0
\end{array}
$$
- Khi đó, sóng điện từ lan truyền với vận tốc 
$$v = \frac{1}{\sqrt{\mu\mu_0\epsilon\epsilon_0}} = \frac{c}{\sqrt{\mu\epsilon}}$$
- Đặt $n = \sqrt{\mu\epsilon}$, giá trị này được gọi là **chiết suất** của môi trường

>[!formula] Phương trình truyền sóng điện từ
>$$\begin{array}{l}
>\vec{\nabla}^2\vec{E}-\frac{1}{v^2}\frac{\partial^2\vec{E}}{\partial t^2} =0 \\
>\vec{\nabla}^2\vec{B}-\frac{1}{v^2}\frac{\partial^2\vec{B}}{\partial t^2} = 0
>\end{array}
>$$
>với $$v = \frac{1}{\sqrt{\mu\mu_0\epsilon\epsilon_0}} = \frac{c}{n}$$

## Tính chất của sóng điện từ
- Tồn tại trong cả chân không và môi trường đồng nhất
- Có tính chất giống ánh sáng
- $\vec{E}$ và $\vec{B}$ luôn dao động cùng pha nhưng có phương vuông góc với nhau và cùng vuông góc với phương truyền sóng
- $\vec{E}, \vec{B}, \vec{v}$ lập thành tam diện thuận

## Năng lượng sóng điện từ
- Mật độ [[nang_luong_dien_truong|năng lượng điện trường]]
$$\omega_E = \frac{1}{2}DE = \frac{1}{2}\epsilon\epsilon_0 E^2$$
- Mật độ [[hien_tuong_tu_cam#Năng lượng từ trường|năng lượng từ trường]]
$$\omega_M = \frac{1}{2}BH = \frac{1}{2}\mu\mu_0H^2$$
- Mật độ năng lượng của điện từ trường
$$\omega = \frac{1}{2}\epsilon\epsilon_0 E^2 + \frac{1}{2}\epsilon\epsilon_0 H^2 (1)$$
- Đối với sóng điện từ, ta có 
$$\sqrt{\epsilon\epsilon_0}E = \sqrt{\mu\mu_0}H (2)$$
Thay (2) vào (1) ta có

>[!formula] Mật độ năng lượng sóng điện từ
>$$\omega = \sqrt{\mu\mu_0\epsilon\epsilon_0}EH = \frac{EH}{v}$$

## Năng thông sóng điện từ

>[!definition] Năng thông
>là năng lượng sóng truyền qua một đơn vị diện tích vuông góc với phương truyền trong một đơn vị thời gian

$$P = \frac{\omega\Delta V}{S\Delta t} = \frac{\omega v S \Delta t}{S \Delta t} = \omega v = EH$$
