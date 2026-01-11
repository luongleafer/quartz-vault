---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 7
unit: 1
title: Bài toán cực tiểu hóa không ràng buộc
---
# Bài toán cực tiểu hóa không ràng buộc
## Nền tảng giải tích

## Các phương pháp cực tiểu một biến
Xét các hàm đơn cực trị $f(x)$ (hàm chỉ có một điểm cực đại/cực tiểu) trên một đoạn xác định, hay:
- $x_1 < x_2 <x^\star \Rightarrow f(x_2) < f(x_1)$
- $x_2 > x_1 > x^\star \Rightarrow f(x_1) < f(x_2)$
với $x^\star$ là điểm cực tiểu

Để tìm cực tiểu của các hàm đơn cực trị, ta dùng thuật toán lặp như sau:
- Từ đoạn xuất phát ban đầu $[a_0;b_0]$
- Xác định hai giá trị trên $[a_0;b_0]$ là $x_1^{(0)}; x_2^{(0)}$.
- Tính $f_1 = f(x_1); f_2 = f(x_2)$
	- Nếu $f_1 < f_2$, đặt $a_1 = a_0; b_1 = x_2$
	- Nếu $f_1 > f_2$, đặt $a_1 = x_1; b_1 = b_0$
	- Nếu $f_1 = f_2$, đặt $a_1 = x_1; b_1 = x_2$
- Nếu $|b_1 - a_1| < 2e$, với $e$ là sai số cho trước, kết thúc thuật toán, ngược lại lặp với đoạn $[a_1;b_1]$ mới

Các phương pháp khác nhau sử dụng các cách chọn $x_1^{(k)}; x_2^{(k)}$ khác nhau.

Phương pháp tìm kiếm thông thường dựa trên phương pháp chia đôi:
$$
\begin{eqnarray}
x_1^{(k)} = a_k + \frac{b_k - a_k}{2} - \frac{e}{2}\\
x_2^{(k)} = a_k + \frac{b_k - a_k}{2} + \frac{e}{2}
\end{eqnarray}
$$
Phương pháp Fibonacci sử dụng dãy Fibonacci:
$$
\begin{array}{l}
F_0 = F_1 = 1\\
F_k = F_{k-1} + F_{k-2} (k\ge 2)
\end{array}
$$
Khi đó
$$
\begin{eqnarray}
x_1^{(k)} = a_k + (b_k - a_k)\frac{F_{N-k-1}}{F_{N-k+1}}\\
x_2^{(k)} = a_k + (b_k - a_k)\frac{F_{N-k}}{F_{N-k+1}}
\end{eqnarray}
$$

Phương pháp lát cắt vàng cải biên dựa trên phương pháp Fibonacci, áp dụng hệ số hằng:
$$
\begin{eqnarray}
x_1^{(k)} = a_k + 0.382(b_k - a_k)\\
x_2^{(k)} = a_k + 0.618(b_k - a_k)
\end{eqnarray}
$$

## Các phương pháp cực tiểu đối với hàm nhiều biến

Xét $f(x): \mathbb{R}^n \to \mathbb{R}$, ta cần tìm $\min f(x)$.
Từ một giá trị $x^0$ ban đầu, ta thực hiện thủ tục lặp:
$$x^{k+1} = x^k + \alpha_k p^k \quad (1)$$
trong đó $p^k$  là _hướng di chuyển_, còn $\alpha_k$ là _độ dài bước dịch chuyển_ theo hướng $p^k$.

### Phương pháp gradient
Để giá trị $f(x^k)$ giảm dần, ta chọn $p^k$ sao cho
$$\left< \nabla f(x^k), p^k \right> < 0$$
Khi đó, ta có thể chọn $p^k = -\nabla f(x^k)$ và $\alpha_k > 0$
Khi đó công thức lặp $(1)$ trở thành
$$x^{k+1} = x^k - \alpha_k \nabla f(x^k) (\alpha_k > 0)$$
Ta có thể chọn $\alpha_k$ bằng một trong hai cách:
- Cách 1: $\alpha_k = \lambda$ với $\lambda$ là giá trị để $f(x^k - \lambda \nabla f(x^k))$ là nhỏ nhất, sử dụng các phương pháp tối thiểu hóa hàm một biến
- Cách 2: 
	- Xét biến $\alpha = \overline{\alpha} >0$ xác định trước
	- Đặt $u = x^k - \alpha \nabla f(x^k)$
	- Nếu $f(u) - f(x^k) \le -\epsilon \alpha ||\nabla f(x^k)||^2$ với một giá trị $0 < \epsilon < 1$ nào đó, thì đặt $\alpha_k = \alpha$. Nếu không, chia đôi $\alpha$ và quay trở lại bước lặp.

### Phương pháp Newton
Nếu $f$ _hai lần khả vi liên tục_, ta có thể sử dụng khai triển Taylor:

$$f_k(x) \approx f'(x^k) + \left< f'(x^k),(x-x^k) \right> + \frac{1}{2} \left< H(x^k)(x-x^k), (x-x^k) \right>$$
Gọi $u^k$ là vector sao cho $f_k(u^k)$ nhỏ nhất, khi đó ta chọn hướng dịch chuyển $p^k = u^k - x^k$ và có công thức lặp 
$$x^{k+1} = x^k + \alpha_k(u^k-x^k)$$
Phương pháp Newton sử dụng $\alpha_k = 1 \forall k$
Khi đó ta có $x^{k+1} = u^k$, tức là
$$f_k(x^{k+1}) = \min f_k(x)$$
Như vậy $x^{k+1}$ là điểm dừng của $f_k(x)$, khi đó
$$\nabla f_k(x^{k+1}) = \nabla f(x^k) + H(x^k)(x^{k+1}-x^k) = 0$$
Vậy ta có thể xác định $x^{k+1}$ dựa theo công thức lặp sau
$$x^{k+1} = x^k - H^{-1}(x^k)\nabla f(x^k)$$
Phương pháp Newton hội tụ với tốc độ bình phương.

### Phương pháp tìm kiếm
Nếu việc tính toán đạo hàm của hàm phức tạp, ta có thể sử dụng phương pháp tìm kiếm, cụ thể như sau:
Xác định bước nhảy ban đầu $\alpha_0$.
Tại bước lặp thứ $k$, đặt $i_k = k \%n + 1$, với toán tử $\%$ biểu thị phép chia lấy dư. Hướng di chuyển $p_k$ là vector cột gồm các số $0$, và giá trị $1$ duy nhất ở hàng thứ $i_k$.
Nếu $f(x^k + \alpha_k p^k) < f(x^k)$ thì đặt
$$x^{k+1} = x^k + \alpha_k p^k$$
và giữ nguyên $\alpha_{k+1} = \alpha_k$. Ngược lại, xét $f(x^k - \alpha_k p^k) < f(x^k)$, nếu đúng thì đặt
$$x^{k+1} = x^k - \alpha_k p^k$$
và giữ nguyên $\alpha_{k+1} = \alpha_k$. Nếu cả hai bất đẳng thức trên đều sai, ta giữ nguyên $x^{k+1} = x^k$, và đặt $a_{k+1} = \lambda a_k$ ($0<\lambda<1$), nếu $i_k = n$ và $x^k = x^{k-n+1}$, ngược lại giữ nguyên $\alpha_{k+1} = \alpha_k$.
Có thể hiểu phương pháp tìm kiếm sẽ giảm lần lượt từng thành phần của $x$ theo chu kì, và chỉ giảm bước nhảy nếu giá trị $x_k$ giữ nguyên trong cả chu kì. 