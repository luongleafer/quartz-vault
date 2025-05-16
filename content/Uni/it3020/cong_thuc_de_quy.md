---
subject: "[[it3020]]"
chapter: 1
unit: 2
title: Công thức đệ quy
tags:
  - university
  - note
published: 2025-04-05
---

# Công thức đệ quy
- Là công thức biểu diễn $a_n$ theo $a_{n-1}, a_{n-2},... a_1$

## Công thức đệ quy tuyến tính thuần nhất hệ số hằng bậc k
Có dạng 
$$a_n = c_1a_{n-1} + c_2a_{n-2} + ... + c_ka_{n-k}$$

Xét **phương trình đặc trưng**
$$r^k - c_1r^{k-1} - c_2r^{k-2} - ... - c_k = 0 (*)$$

- Nếu $(*)$ có k nghiệm phân biệt, ta có công thức tổng quát
$$a_n = \alpha_1 r_1^n + \alpha_2 r_2^n + ... + \alpha_k r_k^n$$
- Nếu $(*)$ có t nghiệm $r_1, r_2, ... r_t$, mỗi nghiệm có bội $m_1, m_2, ... m_t$, ta có công thức tổng quát
$$a_n = P_1r_1^n + P_2r_2^n + ... + P_tr_t^n$$
Với $P_t$ là đa thức bậc $m_t - 1$

## Công thức đệ quy tuyến tính không thuần nhất hệ số hằng
Có dạng
$$a_n = G + F(n)$$
Với $a_n = G$ là công thức đệ quy tuyến tính thuần nhất hệ số hằng

- Nghiệm của công thức có dạng $a_n = a_n^{(p)} + a_n^{(h)}$ với $a_n^{(p)}$ là nghiệm của công thức $a_n = G$
- Nếu $F(n) = P(n) . s^n$ với $P(n)$ là đa thức bậc $t$:
	- Nếu $s$ không phải là nghiệm trong phương trình đặc trưng của $a_n = G$, $a_n^{(h))}$ có dạng giống $Q(n).s^n$ với $Q(n)$ là đa thức bậc $t$
	- Nếu $s$ là nghiệm bội $m$ trong phương trình đặc trưng của $a_n = G$, $a_n^{(h))}$ có dạng giống $n^mQ(n)s^n$