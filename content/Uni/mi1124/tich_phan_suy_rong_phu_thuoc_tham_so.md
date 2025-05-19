---
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 3
unit: 6
title: Tích phân suy rộng phụ thuộc tham số
---

# Tích phân suy rộng phụ thuộc tham số
## Định nghĩa
$$I(y) = \int_a^{+\infty}{f(x;y)dx}$$
## Sự hội tụ, hội tụ đều
- $I(y)$ hội tụ tại $y_0$ nếu $\int_a^{+\infty}{f(x;y_0)dx}$ hội tụ, tức là với mỗi $\epsilon > 0$, tồn tại $b$ phụ thuộc vào $\epsilon$ và $y_0$ sao cho
$$\bigg|\int_A^{+\infty}{f(x;y)dx}\bigg|<\epsilon\, \forall A > b$$
- $I(y)$ hội tụ trên $[c;d]$ nếu nó hội tụ tại mọi điểm trên đó
- $I(y)$ hội tụ đều trên $[c;d]$ nếu với mỗi $\epsilon > 0$, tồn tại $b$ chỉ phụ thuộc vào $\epsilon$ sao cho
$$\bigg|\int_A^{+\infty}{f(x;y)dx}\bigg|<\epsilon\, \forall A > b \, \forall y \in [c;d]$$

>[!formula] Tiêu chuẩn hội tụ Weierstrass
>Nếu $|f(x;y)|\le g(x) \forall (x;y) \in [a;+\infty) \times [c;d]$ và $\int_a^{+\infty}{g(x)\,dx}$ hội tụ trên $[c;d]$ thì $I(y)$ hội tụ đều trên $[c;d]$

## Tính liên tục, khả tích, khả vi
### Tính liên tục, khả tích
- Nếu $f(x;y)$ liên tục trên $[a;+\infty) \times [c;d]$ và $I(y)$ hội tụ đều trên $[c;d]$ thì $I(y)$ liên tục và khả tích trên $[c;d]$
### Tính khả vi
- Nếu $f(x;y)$ và $f'_y(x;y)$ liên tục trên  $[a;+\infty) \times [c;d]$
- $I(y)$ hội tụ, $\int_a^{+\infty}{f'_y(x;y)dx}$ hội tụ đều trên $[c;d]$ thì $I(y)$ khả vi trên $[c;d]$ và
$$I'(y) = \int_a^{+\infty}{f'_y(x;y)dx}$$