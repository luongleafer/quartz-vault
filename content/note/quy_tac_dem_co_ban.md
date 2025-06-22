---
aliases: 
subject: "[[it3020]]"
unit: 1
chapter: 1
title: Các quy tắc đếm cơ bản
subject-code: it3020
tags:
  - university
  - note
share: true
---

# Các quy tắc đếm cơ bản
## Quy tắc cộng

- Cho $A$ và $B$ là hai tập hợp _rời nhau_, ta có:
$$N(A \cup B) = N(A) + N(B)$$
- Mở rộng: cho $A_1$, $A_2$, ... $A_n$ là phân hoạch của A thì:
$$N(A) = \sum_{i=1}^{n}{N(A_i)}$$

## Quy tắc nhân
- Cho bộ hai số có thứ tự $(a;b)$. Nếu $a$ có $m$ cách chọn, $b$ có $n$ cách chọn thì số bộ số $(a;b)$ có thể có là $m \times n$ 
- Mở rộng: cho n tập hợp $A_1$, $A_2$, ... $A_n$ ta có:
$$N(A_1 \times A_2 \times A_3 \times ... \times A_n ) = \prod_{i=1}^n{N(A_i)}$$

## Các cấu hình tổ hợp cơ bản
### Hoán vị
- **Hoán vị** của một tập hợp X là một bộ có thứ tự gồm n thành phần khác nhau đôi một, mỗi thành phần là phần tử của X.
- Số lượng hoán vị của tập có n phần tử: $P_n = n!$
### Chỉnh hợp
- **Chỉnh hợp lặp** chập k của n phần tử là một bộ có thứ tự gồm k thành phần, mỗi thành phần là phần tử của X, các thành phần có thể lặp lại
- Số lượng chỉnh hợp lặp: $A^k_n = n^k$
- **Chỉnh hợp không lặp** chập k của n phần tử là một bộ có thứ tự gồm k thành phần khác nhau đôi một, mỗi thành phần là phần tử của X
- Số lượng chỉnh hợp không lặp: $P^k_n = \frac{n!}{(n-k)!}$
### Tổ hợp
- **Tổ hợp** chập k của n phần tử là một bộ không có thứ tự gồm k thành phần khác nhau đôi một, mỗi thành phần là phần tử của X
- Số lượng tổ hợp: $C^k_n = \frac{n!}{k!(n-k)!)}$

## Nguyên lí bù trừ
- Cho n tập hợp $A_1, A_2,... A_n$, ta có:
$$N(\bigcup_{i=1}^{n}{A_i}) = \sum_{k=1}^{n}{(-1)^{k-1}N_k}$$
$$N_k = \sum_{1\le i_1 < i_2 < ... < i_k \le n}N(\bigcap_{j=1}^{k}A_{i_j})$$