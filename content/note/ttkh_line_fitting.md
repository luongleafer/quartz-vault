---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 3
unit: 3
title: Đường so khớp
---
# Đường so khớp (Line-fitting)
## Đặt vấn đề
- Xét một hàm $f(x)$ không rõ công thức, nhưng biết $n$ giá trị tại $n$ điểm $x_1, x_2,...,x_n$ là $f_1,f_2,...,f_n$
- Ta cần _xấp xỉ_ hàm $f(x)$ bằng một hàm $p(x)$ biểu diễn được dưới dạng giải tích
- Có hai phương pháp thực hiện:
	- **Nội suy (Interpolation)**: $p(x)$ đi qua _tất cả_ các điểm dữ liệu, nói cách khác $p(x_i) = f_i \forall 1 \le i \le n$
	- **Hồi quy (Regression)**: xác định trước dạng của $p(x)$ dưới dạng tham số. Điều chỉnh tham số để một tiêu chí nhất định của $p(x)$ so với $f(x)$ là _nhỏ nhất_
## Nội suy

>[!definition] Định nghĩa nội suy
>Hàm $p(x)$ nội suy bộ dữ liệu ${(x_i;f_i)}, 0 \le i \le n$ nếu $p(x_i) = f_i \forall 0 \le i \le N$

- Trong mục này, ta tìm hiểu nội suy về đa thức do hàm đa thức đơn giản, dễ biểu diễn và lưu trữ.
### Nội suy tuyến tính (Linear Interpolation)
- Trường hợp bộ dữ liệu chỉ có hai điểm, ta có thể dùng nội suy tuyến tính
- Hàm $p(x)$ là đa thức bậc nhất, có dạng $$p(x) = a_0 + a_1x$$
- Ta có
$$
\begin{aligned}
p(x_1) = f_1 = a_0 + a_1x_1\\
p(x_2) = f_2 = a_0 + a_2x_2
\end{aligned}
$$
- Nếu $x_0 \neq x_1$ thì
$$a_0 = \frac{x_1f_0 - x_0f_1}{x_1 - x_0}$$
$$a_1 = \frac{f_1 - f_0}{x_1 - x_0}$$
### Nội suy Lagrange
- Nội suy bộ dữ liệu gồm $N+1$ điểm $(x_0;f_0),(x_1;f_1),...,(x_N;f_N)$ bằng một đa thức bậc không quá $N$.
- Dạng Lagrange của đa thức nội suy:
$$p(x) = f_0V_0(x) + f_1V_1(x) + ... + f_NV_N(x)$$
- Trong đó $V_i(x)$ là các đa thức bậc $N$ thỏa mãn:
$$V_i(x_j) = \begin{cases} 1 \text{    nếu    }i = j \\
0 \text{    nếu    } i \neq j
\end{cases}$$
- Ta có thể xây dựng $V_i$ dưới dạng:
$$V_i = \prod_{j\neq i}\frac{x - x_j}{x_i - x_j}$$
- Vậy ta có: đa thức nội suy Lagrange bộ dữ liệu có dạng
$$p(x) = \sum_{i=0}^n \bigg(f_i \times \prod_{j\neq i}\frac{x - x_j}{x_i - x_j}\bigg)$$
- Họ các $V_i(x)$ được gọi là **họ đa thức cơ sở (Lagrange basis functions)**
- Sai số của nội suy, còn gọi là phần dư Lagrange, có công thức
$$f(x)- p(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}\prod_{i = 0}^n(x-x_i)$$
- Trong đó, $\xi$ trong khoảng từ $x_0$ đến $x_N$, phụ thuộc vào $x$

### Nội suy spline
- Sử dụng các đa thức bậc thấp để xấp xỉ từng đoạn
- Nội suy spline tuyến tính từng khúc:

$$S_{1,N}(x) = \begin{cases}
\frac{f_1 - f_0}{x_1 - x_0}(x - x_1) + f_1 \quad x \in [x_0;x_1] \\
\frac{f_2 - f_1}{x_2 - x_1}(x - x_2) + f_2 \quad x \in [x_1;x_2] \\
...\\
\frac{f_N - f_{N-1}}{x_N - x_{N-1}}(x - x_N) + f_N \quad x \in [x_{N-1};x_N] \\
\end{cases}$$
- Nội suy spline bậc ba
$$S_{3,N}(x) = \begin{cases}
p_1(x) = a_{10} + a_{11}x+a_{12}x^2 + a_{13}x^3 \quad x \in [x_0;x_1] \\
p_2(x) = a_{20} + a_{21}x+a_{22}x^2 + a_{23}x^3 \quad x \in [x_1;x_2] \\
...\\
p_N(x) = a_{N0} + a_{N1}x+a_{N2}x^2 + a_{N3}x^3 \quad x \in [x_{N-1};x_N] \\
\end{cases}$$
- Hàm $S_{3,N}(x)$ cần thỏa mãn các điều kiện sau:
	- Liên tục: $$p_i(x_i) = p_{i+1}(x_i) = f_i (0 \le i < N)$$
	- Đạo hàm bậc 1, bậc 2 liên tục: $$p'_i(x_i) = p'_{i+1}(x_i); p''_i(x_i) = p''_{i+1}(x_i)$$
	- Và một trong 3 điều kiện sau:
		- Điều kiện biên tự nhiên: $$p_1''(x_0) = 0; p_N''(x_N) = 0$$
		- Điều kiện đạo hàm cấp hai: $$p_1''(x_0) = f''(x_0); p_N''(x_N) = f''(x_N)$$
		- Điều kiện sát biên: $$p_1'''(x_1) = p_2'''(x_1); p_{N-1}'''(x_{N-1}) = p_N'''(x_{N-1})$$

## Hồi quy
- Thay vì tìm hàm đi qua chính xác các điểm dữ liệu, hồi quy xây dựng một hàm $y(x)$ (có dạng giải tích xác định) sao cho _sai số là tối thiểu_.
- Xét sai số dưới dạng bình phương nhỏ nhất (least square)
$$E = \sum_{i=1}^N(f_i - y(x_i))^2$$
### Hồi quy tuyến tính (Linear Regression)
- Xét hàm hồi quy $y(x) = mx+b$
- Khi này ta có
$$E = L(m;b) = \sum_{i=1}^N(f_i - (mx_i + b))^2$$
- Ta cần tìm $m$ và $b$ sao cho $L(m;b)$ là nhỏ nhất.
- Do đây là hàm hai biến, xét hàm đạt cực tiểu khi $\frac{\delta L}{\delta m} = 0$ và $\frac{\delta L}{\delta b} = 0$
- Điều kiện trên tương ứng với [[ttkh_linear_equations|hệ phương trình tuyến tính]] sau:
$$\begin{bmatrix}
\sum_{i=1}^N{x_i^2} & \sum_{i=1}^N x_i \\
\sum_{i=1}^N x_i & N
\end{bmatrix} \times \begin{bmatrix} m \\ b \end{bmatrix} = \begin{bmatrix} \sum_{i=1}^N{x_if_i} \\ \sum_{i=1}^N f_i \end{bmatrix}$$
### Hồi quy bậc cao
- Tổng quát hóa phương pháp hồi quy tuyến tính, xét hàm hồi quy $y(x) = a_0 + a_1x + a_2x^2 + ... + a_Mx^M$
- Dựa trên tiêu chí bình phương tối thiểu và thực hiện tương tự hồi quy tuyến tính, đặt
$$s^{(k)} = \sum_{i=1}^N{x_i}^k$$
-Ccác tham số $a_0$ đến $a_M$ là nghiệm của hệ phương trình tuyến tính sau
$$
\begin{bmatrix}
s^{(0)} & s^{(1)} & \dots & s^{(M)} \\
s^{(1)} & s^{(2)} & \dots & s^{(M+1)} \\
\vdots & \vdots & \ddots & \vdots \\
s^{(M)} & s^{(M+1)} & \dots & s^{(2M)}
\end{bmatrix}
\times
\begin{bmatrix}
a_0 \\ a_1 \\ \vdots \\ a_M
\end{bmatrix}
=
\begin{bmatrix}
\sum_{i=1}^N f_i \\
\sum_{i=1}^N f_ix_i \\
\vdots \\
\sum_{i=1}^N f_ix_i^M \\
\end{bmatrix}
$$
