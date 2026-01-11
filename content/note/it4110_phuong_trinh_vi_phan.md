---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 6
unit: 1
title: Bài toán giá trị ban đầu đối với phương trình vi phân
---
# Bài toán giá trị ban đầu đối với phương trình vi phân
## Phương trình vi phân
Một **phương trình vi phân cấp 1** đơn giản có dạng
$$y'(t) = f(y;t)$$
Với $y$ là một hàm phụ thuộc vào $t$, $f$ là hàm hai biến phụ thuộc vào $y$ và $t$.
Để giải phương trình này ta cần các công cụ toán học. Tuy nhiên, nếu ta biết giá trị $y_0 = y(t_0)$ với giá trị $t_0$ nào đó, ta có thể xây dựng các giá trị tiếp theo. Đây được gọi là **bài toán giá trị ban đầu (initial value problem)**.
Vậy một bài toán giá trị ban đầu với phương trình vi phân cấp 1 có thể được phát biểu như sau:
$$\begin{cases}
y'(t) = f(y;t) \\
y_0 = y(t_0)
\end{cases}$$
Nếu $f$ _chỉ phụ thuộc vào $t$_, ta có thể dựng lại các giá trị $y(t)$ bằng [[ttkh_integral_approximation|tích phân]].
Nếu $f$ phụ thuộc vào $y$, ta có một số phương pháp số để _tính gần đúng_ $y(t_n)$ với $t_n = t_0 + nh$. $h$ được gọi là _bước nhảy_. Các phương pháp này thường dùng các công thức [[ttkh_derivative_approximation|xấp xỉ đạo hàm]] hoặc tích phân để xây dựng công thức truy hồi tính $y_{n+1} = y(t_{n+1})$ dựa trên $y_n=y(t_n)$.
## Phương pháp Euler
### Phương pháp Euler thuận
Sử dụng công thức sai phân thuận, xấp xỉ
$$y'(t_n) \approx \frac{y(t_n+h)-y(t_n)}{h} = \frac{y_{n+1} - y_n}{h} = f(y_n;t_n)$$
Khi đó ta có công thức truy hồi để xấp xỉ $y(t)$ như sau:
$$y_{n+1} = y_n + hf(y_n;t_n)$$
Phương pháp Euler thuận dù đơn giản,  nhưng có sai số làm tròn lớn, và không ổn định.
Để ổn định phương pháp Euler thuận, ta có phương pháp Euler cải biên: Sử dụng quy tắc hình thang để tính tích phân:
$$
\begin{aligned}
y_{n+1} &= y_n + \int_{t_n}^{t_{n+1}}y'(t)dt \\ &= y_n + \int_{t_n}^{t_{n+1}}f(y;t)dt \\ &\approx y_n + \frac{h}{2}(f(y_{n+1};t_{n+1}) + f(y_n;t_n))
\end{aligned}$$
Khi đó, để tìm $y_{n+1}$, ta cần [[ttkh_nonlinear_equations|giải phương trình]].

### Phương pháp Euler ngược
Sử dụng công thức sai phân ngược, xấp xỉ
$$y'(t_{n+1}) \approx \frac{y_{n+1}-y_n}{h} = f(y_{n+1};t_{n+1})$$
Khi đó ta có công thức truy hồi
$$y_{n+1} = y_n + hf(y_{n+1};t_{n+1})$$
Và giải phương trình để tìm $y_{n+1}$

## Phương pháp Runge-Kutta
Phương pháp Runge-Kutta sử dụng xấp xỉ theo tích phân
$$y_{n+1} = y_n + \int_{t_n}^{t_{n+1}}f(y;t)dt$$
### Phương pháp Runge-Kutta bậc 2
Sử dụng quy tắc hình thang
$$\int_{t_n}^{t_{n+1}}f(y;t)dt = \frac{h}{2}(f(y_n;t_n) + f(y_{n+1};t_{n+1}))$$
Tuy nhiên, do $y_{n+1}$ chưa biết, ta xấp xỉ $y_{n+1}$ bằng phương pháp Newton:
$$\overline{y_{n+1}} = y_n + h f(y_n;t_n)$$
Khi đó ta có
$$y_{n+1} = y_n + \frac{h}{2}(f(y_n;t_n) + f(\overline{y_{n+1}};t_{n+1}))$$
Độ chính xác của phương pháp Runge-Kutta bậc 2 là $h^2$.

### Phương pháp Runge-Kutta bậc 3
Sử dụng phương pháp Simson 1/3 để xấp xỉ tích phân, ta có
$$y_{n+1} = y_n + \frac{k_1 + 4k_2 + k_3}{6}$$
với
$$\begin{aligned}
k_1 &= hf(y_n;t_n)\\
k_2 &= hf(y_n + \frac{k+1}{2}; t_n + \frac{h}{2}) \\
k_3 &= hf(y_n + \theta k_1 + (1-\theta)k_2; t_n + h)
\end{aligned}$$
với giá trị $\theta$ tối ưu là $\theta = -1$

### Phương pháp Runge-Kutta bậc 4
Dựa trên Simson 1/3
$$y_{n+1} = y_n + \frac{k_1+2k_2+2k_3+k_4}{6}$$
với
$$\begin{aligned}
k_1 &= hf(y_n;t_n)\\
k_2 &= hf(y_n + \frac{k_1}{2}; t_n + \frac{h}{2}) \\
k_3 &= hf(y_n + \frac{k_2}{2};t_n + \frac{h}{2})\\
k_4 &= hf(y_n+k_3;t_n+h)
\end{aligned}$$
Dựa trên Simson 3/8
$$y_{n+1} = y_n + \frac{k_1 + 3k_2 + 3k_3 + k_4}{8}$$
với
$$
\begin{aligned}
k_1 &= hf(y_n;t_n)\\
k_2 &= hf(y_n + \frac{k_1}{3}; t_n + \frac{h}{3}) \\
k_3 &= hf(y_n + \frac{k_1}{3} + \frac{k_2}{3};t_n + \frac{2h}{3})\\
k_4 &= hf(y_n+k_1-k_2+k_3;t_n+h)
\end{aligned}
$$
