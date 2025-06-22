---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 3
unit: 5
title: Tích phân xác định phụ thuộc tham số
share: true
---

# Tích phân xác định phụ thuộc tham số
## Định nghĩa

Xét hàm $f(x;y)$ liên tục trên $[a;b]\times[c;d]$ Khi đó hàm số
$$I(y) = \int_a^b{f(x;y)\,dx}$$ là tích phân xác định phụ thuộc tham số

## Tính chất
### Tính liên tục
- Nếu $f(x;y)$ liên tục trên $[a;b]\times[c;d]$ thì $I(y)$ liên tục trên $[c;d]$
### Tính khả tích
- Nếu $f(x;y)$ liên tục trên $[a;b]\times[c;d]$ thì $I(y)$ khả tích trên $[c;d]$
$$\int_c^d{I(y)\,dy} = \iint_D{f(x;y)\,dxdy}$$
### Tính khả vi
- Nếu $f(x;y)$ liên tục trên $[a;b]\times[c;d]$, và
- $f'_y(x;y)$ liên tục trên $[a;b]\times[c;d]$ thì $I(y)$ khả vi trên $[c;d]$
$$I'(y) = \int_a^b{f'_y(x;y)\,dx}$$

## Trường hợp cận biến đổi
Xét
$$I(y) = \int_{a(y)}^{b(y)}{f(x;y)dx}$$

### Tính liên tục, khả tích
- Nếu $f(x;y)$ liên tục trên $[a;b]\times[c;d]$
- $a(y), b(y)$ liên tục trên $[c;d]$
- $a \le a(y), b(y) \le b(y) \forall y\in [c;d]$
- Thì $I(y)$ liên tục, và khả tích trên $[c;d]$

### Tính khả vi
- Nếu $f(x;y)$ và $f'_y(x;y)$ liên tục trên $[a;b]\times[c;d]$
- $a(y); b(y)$ khả vi trên $[c;d]$
- Thì $I(y)$ khả vi trên $[c;d]$ và
$$I'(y) = \int_{a(y)}^{b(y)}{f'_y(x;y)\,dx} + f\big(b(y),y\big)b'(y) - f\big(a(y),y\big)a'(y)$$