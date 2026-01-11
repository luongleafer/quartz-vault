---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 1
unit: 2
title: Định nghĩa xác suất
---
# Định nghĩa xác suất
## Định nghĩa cổ điển
- Xét [[phep_thu_su_kien|phép thử]] có _hữu hạn_ kết cục đồng khả năng. 
- Xác suất của sự kiện $A$ được định nghĩa là tỉ số giữa số kết cục có lợi cho $A$, trên tổng số kết cục của phép thử
$$P(A) = \frac{|A|}{|\Omega|}$$
- Ví dụ: Một hộp có 10 quả bóng gồm 1 bóng đỏ, 2 bóng xanh, 3 bóng vàng, 4 bóng trắng. Xét phép thử "Lấy ngẫu nhiên một quả bóng" và sự kiện A: "Quả bóng lấy được màu vàng". Xác suất của sự kiện
$$P(A) = \frac{|A|}{|\Omega|} = \frac{3}{10}$$
## Định nghĩa thống kê
- Tiến hành _hàng loạt_ $n$ phép thử cùng loại. Khi tiến hành, sự kiện $A$ xảy ra $m$ lần.
- $m$ được gọi là **tần số** của sự kiện $A$, tỉ số $\frac{m}{n}$ được gọi là **tần suất** xuất hiện $A$.
- Xác suất của sự kiện $A$ được định nghĩa là tần suất xuất hiện của $A$, khi số lần thực hiện phép thử tiến đến vô cùng
$$P(A) = \lim_{n \to \infty}\frac{m}{n}$$
- Ví dụ: Khi ta tung đồng xu nhiều lần, ta nhận thấy số lần xuất hiện mặt ngửa xuất hiện trong một nửa số lần tung đồng xu. Khi này ta kết luận, xác suất của sự kiện "Đồng xu xuất hiện mặt ngửa" là $\frac{1}{2} = 0,5$

## Tính chất của xác suất
Xét $A$, $B$ là hai sự kiện, ta có
$$0 \le P(A) \le 1$$
$$P(\Omega) = 1, P(\emptyset) = 0$$
Nếu $A$, $B$ xung khắc: $$P(A+B) = P(A) + P(B)$$
$$P(\overline{A}) = 1 - P(A)$$
$$A \subseteq B \Rightarrow P(A) \le P(B)$$
