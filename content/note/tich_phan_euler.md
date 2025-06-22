---
aliases: 
tags:
  - university
  - note
subject: "[[mi1124]]"
chapter: 3
unit: 7
title: Tích phân Euler
share: true
---

# Tích phân Euler
## Hàm gamma
$$\Gamma(p) = \int_0^{+\infty}{x^{p-1}e^{-x}\,dx}$$
- Tập xác định $(0;+\infty)$
- Giá trị đặc biệt: $\Gamma(1) = 1$ , $\Gamma(\frac{1}{2}) = \sqrt{\pi}$
- Một số tính chất
$$\Gamma(p+1)= p\Gamma(p)$$
$$\Gamma(n) = (n-1)! (n\in \mathbb{N})$$
$$\Gamma(n+\frac{1}{2}) = \frac{(2n-1)!!}{2^n}\sqrt{\pi}$$
$$\Gamma(p)\Gamma(1-p) = \frac{\pi}{\sin(p\pi)}(0<p<1)$$
## Hàm beta
- Dạng 1: 
$$B(p,q) = \int_0^1{x^{p-1}(1-x)^{q-1}\,dx}$$
- Dạng 2:
$$B(p,q) = \int_0^{+\infty}\frac{x^{p-1}}{(1+x)^{p+q}}\,dx$$
- Liên hệ giữa hàm gamma và beta
$$B(p,q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}$$