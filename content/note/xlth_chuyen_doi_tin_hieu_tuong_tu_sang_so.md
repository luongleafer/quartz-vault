---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 1
unit: 2
title: Chuyển đổi tín hiệu từ tương tự sang số
---
# Chuyển đổi tín hiệu từ tương tự sang số.
## Quá trình chuyển đổi tín hiệu tương tự sang tín hiệu số.
Do tín hiệu tương tự khó làm việc và lưu trữ, ta cần chuyển chúng sang tín hiệu số. Việc chuyển tín hiệu từ tương tự sang số được thực hiện thông qua hai bước:
- Lấy mẫu: tín hiệu được đo ở một số lần nhất định.
- Lượng tử hóa: các giá trị thực của tín hiệu được đưa về các giá trị định mức sẵn.
Kết quả thu được là một tín hiệu rời rạc cả về thời gian và biên độ. Tín hiệu dạng này có thể được lưu trữ và xử lí hiệu quả bằng máy tính.

## Quá trình lấy mẫu
Giả sử ta có một tín hiệu liên tục $x_a(t)$. Việc lấy mẫu được thực hiện tuần hoàn, với mỗi lần lấy mẫu cách nhau một khoảng thời gian được gọi là **Chu kỳ lấy mẫu**, kí hiệu $T_S$. Các giá trị thu được là giá trị của $x_a(t)$ tại các thời điểm $nT_S$, với $n$ là số nguyên. Tần số lấy mẫu, theo đó là $F_S=\frac{1}{T_S}$.

Nếu tín hiệu tương tự là tín hiệu tuần hoàn với tần số $F$, giả sử $x_a(t) = A\cos(2\pi F t + \theta)$. Khi đó tín hiệu thu được qua quá trình lấy mẫu là
$$
\begin{aligned}
x(n) &= x_a(nT_S) \\
&= A\cos(2\pi F nT_S + \theta) \\
&= A\cos(2\pi \frac{F}{F_S}n + \theta)
\end{aligned}
$$
Vậy ta có tần số của tín hiệu rời rạc thu được là $f = \frac{F}{F_S}$
Mỗi giá trị $x(n)$ tại một giá trị $n$ nhất định được gọi là một **mẫu**
## Quá trình lượng tử hóa
Sau quá trình lấy mẫu, ta thu được tín hiệu rời rạc về thời gian, nhưng giá trị của mỗi mẫu là giá trị liên tục. Để lưu trữ một cách thuận tiện, ta cần đưa các giá trị liên tục này về các giá trị rời rạc định mức trước. Từng mức giá trị được định nghĩa này là một **mức lượng tử (quantization level)**. Khoảng cách giữa hai mức lượng tử gần nhất được gọi là một **bước lượng tử (quantization step)**, kí hiệu $\Delta$. _Ví dụ_: nếu ta sử dụng tập hợp $\{0.1,0.2,0.3,0.4,0.5,0.6,0.7,0.8,0.9,1.0\}$, ta có 10 mức lượng tử và bước lượng tử là $0.1$

Mỗi giá trị liên tục của mẫu sẽ được đưa về _mức lượng tử gần nhất_. Ví dụ với 10 mức lượng tử trên, giá trị $0.77$ sẽ được đưa về $0.8$.

Sự chênh lệch giữa giá trị thực và giá trị sau lượng tử hóa được gọi là **lỗi lượng tử**. Nếu gọi $x_q(n)$ là giá trị sau lượng tử hóa và $x(n)$ là giá trị gốc, lỗi lượng tử được kí hiệu là $e_q(n)$ và
$$e_q(n) = x_q(n) - x(n)$$
Khi đó ta luôn có
$$\frac{-\Delta}{2} \le e_q(n) \le \frac{\Delta}{2}$$
Khi đó, công suất lỗi trung bình của tín hiệu trên đoạn $[-\tau,\tau]$ là
$$P_q = \frac{1}{2\tau}\int_{-\tau}^{\tau}e_q^2(t)dt$$
Gọi công suất trung bình của tín hiệu là $P_x$, ta có
$$P_x = \frac{1}{2T_p}\int_{-T_p}^{T_p}x_a^2(t)dt$$
Tỉ số giữa $P_x$ và $P_q$ được gọi là **Signal-to-quantization noise ratio**.

## Định lý lấy mẫu Nyquist-Shannon

Gọi $F_S$ là tần số lấy mẫu cho tín hiệu $x$. Nếu $x$ gồm nhiều tín hiệu có tần số khác nhau hợp thành, định lý lẫy mẫu Nyquist-Shannon chỉ ra rằng, để tránh hiện tượng trùm phổ (aliasing), tần số lấy mẫu gần lớn hơn hoặc bằng 2 lần tần số lớn nhất của tín hiệu, nói cách khác

$$F_S \ge 2\max(f_x)$$
