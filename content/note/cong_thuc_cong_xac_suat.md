---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 1
unit: 3
title: Công thức cộng xác suất
---
# Công thức cộng xác suất
## Đối với hai sự kiện
- Xét hai [[phep_thu_su_kien|sự kiện]] $A$ và $B$. [[dinh_nghia_xac_suat|Xác suất]] của sự kiện $A+B$ được tính theo công thức sau:
$$P(A+B) = P(A) + P(B) - P(AB)$$
- Hệ quả:
	- Công thức phần bù: $P(\overline{A}) = 1 - P(A)$
	- $P(A\overline{B}) = P(A) - P(AB)$

## Đối với nhiều sự kiện
- Xét tập hợp có $n$ sự kiện $A_1, A_2, ... A_n$. Xác suất của sự kiện hợp:
$$P(\bigcup_{i = 1}^n{A_i}) = \sum_{i = 1}^nP(A_i) - \sum_{0<i<j\le n}P(A_iA_j) + ... + (-1)^k\sum_{0<i_1<i_2<...<i_k\le n}{P(\bigcap_{j=1}^k A_j)} + ...$$
- Ví dụ với $n = 3$:
$$P(A_1 + A_2 + A_3) = P(A_1) + P(A_2) + P(A_3) - [P(A_1 A_2)+P(A_2 A_3) + P(A_1 A_3)] + P(A_1 A_2 A_3)$$
