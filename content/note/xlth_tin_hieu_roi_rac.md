---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 1
unit: 3
title: Tín hiệu rời rạc
---
# Tín hiệu rời rạc
Tín hiệu rời rạc là [[xlth_khai_niem_co_ban|tín hiệu]] rời rạc về mặt thời gian và giá trị. Tín hiệu rời rạc thường được thu thập qua việc [[xlth_chuyen_doi_tin_hieu_tuong_tu_sang_so|lấy mẫu và lượng tử hóa]] tín hiệu tương tự.

## Các dạng biểu diễn tín hiệu rời rạc.

Một tín hiệu rời rạc có thể được cho bằng đồ thị, trong đó một trục biểu thị thứ tự mẫu, và trục còn lại là giá trị mẫu, ví dụ
![[Pasted image 20251203160116.png]]
Ngoài ra tín hiệu rời rạc có thể được biểu diễn bằng một hàm số có đối số là số nguyên
$$x(n) = \begin{cases}
1 \quad (n = 1, 3)\\
2 \quad (n = 2) \\
0 \quad \text{giá trị khác}
\end{cases}$$
Tín hiệu rời rạc cũng có thể được liệt kê theo bảng số, dãy số.
Trong máy tính, tín hiệu rời rạc có thể được biểu diễn và lưu trữ trong mảng.

## Một số tín hiệu rời rạc cơ bản
Xung đơn vị:
$$\delta(n) = \begin{cases}
1 \quad n = 0 \\
0 \quad n \neq 0
\end{cases}$$
Dãy xung nhảy bậc đơn vị
$$u(n) = \begin{cases}
1 \quad n \ge 0 \\
0 \quad n < 0
\end{cases}$$
Dãy xung chữ nhật
$$\mathrm{rect}_N(n) = \begin{cases}
1 \quad n = 0 \le n \le N-1 \\
0 \quad n <0 \,\text{hoặc}\, n \ge N
\end{cases}$$
Dãy gốc đơn vị
$$u_r(n) = \begin{cases}
n \quad n \ge 0 \\
0 \quad n < 0
\end{cases}$$
## Một số tính chất và đại lượng của tín hiệu rời rạc
### Năng lượng, công suất của tín hiệu
Năng lượng của tín hiệu
$$E = \sum_{n=-\infty}^{\infty}{|x(n)|^2}$$
Công suất của tín hiệu
$$P = \lim_{N\to\infty}\bigg(\frac{1}{2N+1}\sum_{n=-N}^N|x(n)|^2\bigg)$$
### Một số loại tín hiệu đặc biệt
Một tín hiệu $x(n)$ được gọi là **tín hiệu tuần hoàn** với chu kì $N >0$ nếu $$x(n+N) = x(n) \quad \forall n$$
Một tín hiệu tuần hoàn có thể có nhiều chu kì, chu kì nhỏ nhất được gọi là **chu kì cơ bản**.

Một tín hiệu $x(n)$ được gọi là **tín hiệu chẵn** nếu $$x(-n) = x(n) \quad \forall n$$
Một tín hiệu được gọi là **tín hiệu lẻ** nếu $$x(-n) = -x(n) \quad \forall n$$
Nhận xét: mọi tín hiệu đều có thể được tách thành hai thành phần, gồm một tín hiệu chẵn và một tín hiệu lẻ, thật vậy:
$$x(n) = \bigg(\frac{x(n) + x(-n)}{2}\bigg) + \bigg(\frac{x(n) - x(-n)}{2}\bigg)$$
Dễ thấy $\frac{x(n) + x(-n)}{2}$ là tín hiệu chẵn, còn $\frac{x(n) - x(-n)}{2}$ là tín hiệu lẻ

## Các phép toán cơ bản với tín hiệu rời rạc
### Các phép toán
- **Phép cộng** hai tín hiệu: Cho $x(n)$ và $y(n)$ là hai tín hiệu rời rạc, định nghĩa $z(n) = x(n) + y(n)$ là tín hiệu rời rạc sao cho
$$z(i) = x(i) + y(i) \quad \forall i$$
- **Phép nhân** hai tín hiệu: Cho $x(n)$ và $y(n)$ là hai tín hiệu rời rạc, định nghĩa $z(n) = x(n).y(n)$ là tín hiệu rời rạc sao cho
$$z(i) = x(i)y(i)\quad \forall i$$
- Phép nhân một tín hiệu với đại lượng vô hướng: Cho $x(n)$ là một tín hiệu rời rạc, và $\alpha$ là một số, định nghĩa $y(n) = \alpha x(n)$ là một tín hiệu rời rạc sao cho
$$y(i) = \alpha x(i) \quad \forall i$$
- Phép dịch một tín hiệu sang phải: Cho $x(n)$ là một tín hiệu rời rạc, định nghĩa $y(n) = x(n-n_0)$ là một tín hiệu rời rạc. Tín hiệu được gọi là trễ (muộn) hơn $x(n)$ một khoảng $n_0$ mẫu.
- Phép dịch một tín hiệu sang trái: $z(n) = x(n+n_0)$ là một tín hiệu rời rạc, nhanh (sớm) hơn $x(n)$ một khoảng $n_0$ mẫu.
- Phép đảo trục: $y(n) = x(-n)$ là một tín hiệu rời rạc.
### Phân tích tín hiệu
Sử dụng phép dịch tín hiệu và phép trễ, ta có thể phân tích mọi tín hiệu thành tổng của các tín hiệu xung đơn vị. Thật vậy, gọi $x_k$ là giá trị của $x(n)$ tại mẫu thứ $k$.
Ta có: $\delta(n)$ chỉ nhận giá trị 1 tại $n=0$. Thực hiện phép dịch phải trên tín hiệu xung đơn vị, ta có $\delta(n-k) =1$ chỉ tại $n=k$.
Khi đó một tín hiệu $x(n)$ có thể được phân tích như sau:
$$x(n) = \sum_{k = -\infty}^\infty x_k \delta(n-k)$$
