---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 2
unit: 11
title: Năng lượng điện trường
---

# Năng lượng điện trường
## Năng lượng tương tác của hệ điện tích điểm
- Đặt $q_2$ trong [[dien_truong 1|điện trường]] của $q_1$, [[dien_the 1#^thenang|thế năng]] của $q_2$ trong điện trường của $q_1$ cũng bằng thế năng của $q_1$ trong điện trường của $q_2$
$$W_t = \frac{q_1q_2}{4\pi\epsilon\epsilon_0r}$$
Ta có thể tách thành
$$W_t = \frac{1}{2}q_1\frac{q_2}{4\pi\epsilon\epsilon_0 r} + \frac{1}{2}q_2\frac{q_1}{4\pi\epsilon\epsilon_0 r} = \frac{1}{2}q_1V_1 + \frac{1}{2}q_2V_2$$
Trong đó $V_1$ là điện thế do $q_2$ gây ra tại điểm đặt $q_1$ và $V_2$ là điện thế do $q_1$ gây ra tại điểm đặt $q_2$
- Xét hệ $n$ điện tích điểm
$$W = \frac{1}{2}\sum_{i=1}^{n}{q_iV_i}$$
Trong đó $V_i$ là điện thế do các điện tích điểm còn lại gây ra tại điểm đặt $q_i$
## Năng lượng của [[vat_dan|vật dẫn]] cô lập tĩnh điện
- Điện tích $Q$, điện thế $V$
- Do vật dẫn đẳng thế nên $V_i = V$ với mọi i
- $\sum_{i=1}^{n}q_i = Q$

>[!formula] Năng lượng của vật dẫn cô lập tĩnh điện
>$$W = \frac{1}{2}QV = \frac{1}{2}CV^2 = \frac{1}{2}\frac{Q^2}{C}$$

## Năng lượng của tụ điện
- Tụ điện gồm hai vật dẫn $(Q_1;V_1)$ và $(Q_2;V_2)$
- Do $Q_1 = -Q_2$ nên ta có
$$W = \frac{1}{2}Q_1V_1 + \frac{1}{2}Q_2V_2 = \frac{1}{2}Q(V_1-V_2) = \frac{1}{2}QU$$

>[!formula] Năng lượng của tụ điện
>$$W = \frac{1}{2}QU = \frac{1}{2}CU^2 = \frac{1}{2}\frac{Q^2}{C}$$

## Năng lượng của điện trường bất kì
### Mật độ năng lượng điện trường
- Xét tụ điện phẳng, ta có
$$W = \frac{1}{2}CU^2 = \frac{1}{2}\frac{\epsilon\epsilon_0S}{d}U^2 = \frac{1}{2}\bigg(\frac{\epsilon\epsilon_0U}{d}\bigg)\bigg(\frac{U}{d}\bigg)(Sd) = \frac{1}{2}DEV$$
- Mật độ năng lượng điện trường là năng lượng điện trường trên một đơn vị thể tích:
$$\omega_E = \frac{W}{V} = \frac{1}{2}DE$$

>[!formula] Mật độ năng lượng điện trường
>$$\omega_E = \frac{1}{2}DE$$

### Năng lượng của điện trường bất kì
- Xét điện trường bất kì $E$
- Chia điện trường này thành các vùng không gian vô cùng nhỏ $dV$ mà ở đó _điện trường đều_
- Ta có, vi phân năng lượng điện trường $dW = \omega_e\,dV = \frac{1}{2}DE\,dV$

Vậy ta có
>[!formula] Năng lượng của điện trường bất kì
>$$W = \int_{V}{\frac{1}{2}DE \, dV}$$