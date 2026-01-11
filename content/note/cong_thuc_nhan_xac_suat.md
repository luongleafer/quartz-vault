---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 1
unit: 4
title: Công thức nhân xác suất
---
# Công thức nhân xác suất
## Xác suất có điều kiện
- Xét hai [[phep_thu_su_kien|sự kiện]] $A$ và $B$.
- Ta gọi [[dinh_nghia_xac_suat|xác suất]] của $A$ với điều kiện $B$ là xác suất của $A$ khi ta biết $B$ đã xảy ra, kí hiệu là $P(A | B)$

>[!formula] Công thức xác suất có điều kiện
>$$P(A | B) = \frac{P(AB)}{P(B)}$$

- Xác suất có điều kiện tuân theo các [[dinh_nghia_xac_suat#Tính chất của xác suất|tính chất của xác suất]]

## Công thức nhân xác suất

>[!formula] Công thức nhân xác suất với hai sự kiện
>$$P(AB) = P(B)P(A|B) = P(A)P(B|A)$$

>[!formula] Công thức nhân xác suất tổng quát
>$$P(A_1A_2...A_n) = P(A_1)P(A_2|A_1)P(A_3|A_1A_2)...P(A_n|A_1A_2...A_{n-1})$$

## Sự kiện độc lập
- Hai sự kiện $A$ và $B$ được gọi là **độc lập** nếu sự kiện này không ảnh hưởng đến xác suất xảy ra của sự kiện khác, hay
$$P(A|B) = P(A); P(B|A) = P(B)$$
- Khi đó
$$P(AB) = P(A)P(B)$$
- Tập hợp $\{A_1; A_2;...;A_n\}$ được gọi là _độc lập từng đôi_ nếu $P(A_iA_j) = P(A_i)P(A_j) \forall i \neq j$
- Tập hợp $\{A_1;A_2;...;A_n\}$ được gọi là _độc lập tổng thể_ nếu $P(A_iA_{i+1}...A_{j}) = P(A_i)P(A_{i+1})...P(A_j) \forall 0<i <j\le n$