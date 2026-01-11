---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 5
unit: 1
title: Tính gần đúng đạo hàm
---
# Tính gần đúng đạo hàm
## Tính gần đúng đạo hàm cấp một
- Công thức sai phân thuận

	- $$f'(x) \approx \frac{f(x+h) - f(x)}{h}$$
	- Sai số rút gọn: $$f''(c)\frac{h}{2} = O(h) (x \le c \le x+h)$$
	- Sai số tổng nhỏ nhất khi $$h \approx \sqrt{\epsilon}$$
- Công thức sai phân ngược
	- $$f'(x) \approx \frac{f(x) - f(x-h)}{h}$$
	- Sai số tương tự công thức sai phân thuận
- Công thức sai phân trung tâm
	- $$f'(x) \approx \frac{f(x+h) - f(x-h)}{2h}$$
	- Sai số rút gọn: $$\frac{-1}{6}f^{(3)}(c)h^2 (c \in [x-h,x+h]$$
	- Sai số tổng cộng nhỏ nhất khi $$h \approx \epsilon^{\frac{1}{3}}$$
## Tính gần đúng đạo hàm cấp hai
$$f''(x) = \frac{f(x+h) - 2f(x) + f(x-h)}{h^2}$$
- Sai số rút gọn
$$\frac{-1}{12}f^{(4)}(c) h^2 \quad (c \in [x-h;x+h])$$
