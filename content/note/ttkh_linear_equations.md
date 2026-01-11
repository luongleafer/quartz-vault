---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 2
unit: 2
title: Giải hệ phương trình tuyến tính
---
# Giải hệ phương trình tuyến tính
## Khái niệm hệ phương trình tuyến tính
- Xem thêm: [[Ch2_B07_Hệ_phương_trình_tuyến_tính|Hệ phương trình tuyến tính]]
- Là hệ
$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n &= b_1\\
a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n &= b_2\\
... \\
a_{m1}x_1 + a_{m2}x_2 + ... + a_{mn}x_n &= b_m\\
\end{aligned}
$$
- Ta có thể biểu diễn hệ trên dưới dạng ma trận
$$Ax=b$$
- Với :
	- $A = [a_{ij}]$, được gọi là **ma trận hệ số**.
	- $b = [b_1 b_2 ... b_m]^T$ được gọi là **vector vế phải**
	- $x = [x_1 x_2 ... x_n]^T$ được gọi là **vector vế trái**
- Để giải hệ phương trình tuyến tính, ta có thể:
	- Sử dụng ma trận nghịch đảo nếu $A$ là ma trận vuông không suy biến:
	- $$x = bA^{-1}$$
	- Tuy nhiên cách này không cho độ chính xác cao.
## Giải hệ phương trình tuyến tính bằng phân tích LU
- Xét hệ phương trình có ma trận hệ số là ma trận vuông
### Quá trình khử xuôi
- Là quá trình chuyển ma trận hệ số về dạng tam giác.
- Quá trình này gồm $n-1$ bước.
- Tại bước thứ $k$:
	- Giữ nguyên hàng $k$
	- Với các hàng $j$ từ $k+1$ đến $n$:
		- Chọn nhân tử là $l_{jk} = \frac{a_{jk}}{a_{kk}}$
		- Đặt $row_j = row_j - row_k \times l_{jk}$
- Sau quá trình trên, ta thu được một ma trận tam giác trên có dạng sau
$$
\begin{bmatrix}
a_{11}&a_{12}&a_{13}&...&a_{1n}\\
0&a_{22}&a_{23}'&...&a_{2n}'\\
\vdots&\vdots&\vdots&\ddots&\vdots\\
0&0&0&...&a_{nn}
\end{bmatrix}
$$
- Hệ phương trình của chúng ta giờ có dạng
$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n &= b_1\\
a_{22}x_2 + ... + a_{2n}'x_n &= b_2'\\
... \\
a_{nn}'x_n &= b_n'\\
\end{aligned}
$$
- Để biểu diễn toán học quá trình này, gọi $U$ là ma trận tam giác trên thu được, $L$ là ma trận
$$L_{jk} = \begin{cases}
l_{jk} \text{   nếu   } j < k\\
1 \text{   nếu   } j = k\\
0 \text{   nếu   } j > k
\end{cases}$$
- Ta có
$$LU = A$$
### Quá trình thế ngược
- Ta bắt đầu đi từ dưới lên,
$$x_n = \frac{b'_n}{a_{nn}'}$$
- Thế giá trị $x_n$ trên vào phương trình thứ $n-1$ để tìm $x_{n-1}$, sau đó lấy $x_n$ và $x_{n-1}$ thế vào phương trình thứ $n-2$ để tìm $x_{n-2}$,... Lặp lại cho đến khi đã tìm được tất cả các giá trị của biến.
### Phần tử trụ
- Ở mỗi bước của cả quá trình khử xuôi và thế ngược, ta đều thực hiện phép chia cho các phần tử nằm trên đường chéo chính của ma trận hệ số.
- Nếu phần tử trụ nhỏ hoặc gần 0, việc chia có thể xảy ra sai số lớn khi làm tròn.
- Để tránh việc này, ở mỗi bước, ta cần chọn _phần tử trụ lớn nhất_ bằng cách _hoán vị_ hai hàng của ma trận với nhau. Cụ thể, tại bước thứ $k$ của bước khử xuôi, ta tìm giá trị $a_{jk}$ lớn nhất với $k \le j \le n$ và hoán vị hàng $j$ và hàng $k$.
- Kí hiệu $P_k$ là ma trận thu được nếu hoán vị ma trận đơn vị cấp $n$ theo cách như trên, còn được gọi là **ma trận hoán vị**. Việc hoán vị tạo ra ma trận $A' = P_kA$
- Ở mỗi bước của khử xuôi, nếu thực hiện hoán vị, ta cần đổi chỗ hai phần tử $L_{jk}$ và $L_{kk}$ cho nhau trong ma trận $L$ cuối cùng

### Phân tích LU

>[!formula] Phân tích LU
>Với $A$ là ma trận vuông, ta có thể phân tích A dưới dạng:
>$$LU = PA$$
>Với $L$ là ma trận tam giác dưới, $U$ là ma trận tam giác trên, $P$ là ma trận hoán vị

Ví dụ:
Xét hệ phương trình
$$
\begin{aligned}
5x_1 - 2x_2 + 4x_3 &=15 \\
-3x_1 + 7x_2 + x_3 &= -9\\
2x_1 + 6x_2 - 8x_3 &= 22
\end{aligned}
$$
Ta có ma trận $A$:
$$
A = \begin{bmatrix}
5 & -2 & 4\\
-3 & 7 & 1\\
2 & 6 & -8\\
\end{bmatrix}
$$
- Bước khử xuôi:
	- Xét hàng 1, phần tử trụ $a_{11}=5$ là lớn nhất, ta có $$l_{21} = \frac{-3}{5}; l_{31} = \frac{2}{5}$$
	- Thực hiện biến đổi: $$A = \begin{bmatrix} 5 & -2 &4\\0 &\frac{29}{5} & \frac{17}{5} \\ 0 & \frac{34}{5} & \frac{-48}{5}\end{bmatrix}; B = \begin{bmatrix}15 \\0 \\ 16\end{bmatrix}$$
	- Xét hàng 2, phần tử trụ $a_{22} = \frac{29}{5}$ chưa phải lớn nhất, thực hiện hoán vị hàng 2 và 3, ta có $$A = \begin{bmatrix} 5 & -2 &4\\0 &\frac{34}{5} & \frac{-48}{5} \\ 0 & \frac{29}{5} & \frac{17}{5}\end{bmatrix}; B = \begin{bmatrix}15 \\16 \\ 0\end{bmatrix}$$
	- Khi này ta có $$l_{32} = \frac{29}{34}$$
	- Thực hiện biến đổi: $$A = \begin{bmatrix} 5 & -2 &4\\0 &\frac{34}{5} & \frac{-48}{5} \\ 0 & 0 & \frac{197}{17}\end{bmatrix}; B = \begin{bmatrix}15 \\ 16 \\ \frac{-232}{17}\end{bmatrix}$$
- Từ đó ta có
$$L = \begin{bmatrix}1 & 0 & 0 \\ \frac{2}{5} & 1 & 0 \\ \frac{-3}{5} & \frac{29}{34} & 1\end{bmatrix}; U = \begin{bmatrix}5 & -2 & 4 \\ 0& \frac{34}{5}  & \frac{-48}{5} \\ 0& 0& \frac{197}{17}\end{bmatrix}; P = \begin{bmatrix}1 & 0 & 0 \\ 0& 0  & 1 \\ 0& 1& 0\end{bmatrix}$$
- Bước thế ngược:
$$x_3 = \frac{-232}{17}/ \frac{197}{17} = \frac{-232}{197}$$
$$x_2 = \bigg(16 - \bigg(\frac{-48}{5}\bigg)x_3\bigg)/\frac{34}{5} = \frac{136}{197}$$
$$x_1 = \frac{15 - 4x_3 -(-2)x_2}{5} = \frac{831}{197} $$
## Hệ xác định tồi và số điều kiện của ma trận
### Chuẩn vector
- Xét một [[Ch3_B08_Không_gian_vector|không gian vector]] $S\subseteq \mathbb{R}^n$, chuẩn của vector là một hàm gán mỗi vector $x$ cho một số thực $v(x)$ sao cho:
	- $v(x) \ge 0 \forall x \in S$, $v(x) = 0 \Leftrightarrow x = 0$
	- $v(\alpha x) = |\alpha|x \forall x \in S, \alpha \in \mathbb{R}$
	- $v(x+y) \le v(x) + v(y) \forall x, y \in S$
- Kí hiệu của chuẩn: $||x||$
- Một số chuẩn tiêu biểu:
	- $$||x||_2 = \sqrt{\sum_{i = 1}^n{x_i^2}}$$
	- $$||x||_1 = \sum_{i=1}^n{|x_i|}$$
	- $$||x||_\infty = \max_{1\le i \le n}|x_i|$$
	- $$||x||_p = \bigg(\sum_{i=1}^n|x_i|^p\bigg)^\frac{1}{p}$$
- Chuẩn của một ma trận $A$ được định nghĩa theo chuẩn ma trận:
$$||A|| = \max_{||x|| = 1}||Ax||$$
- Tính chất của chuẩn ma trận:
	- $||A||\ge 0$, $||A = 0||\Leftrightarrow A = 0$
	- $||\alpha A|| = |\alpha| ||A|| (\alpha \in \mathbb{R})$
	- $||A + B|| \le ||A|| + ||B||$
	- $||AB|| \le ||A|| \times ||B||$
	- $||Ax|| \le ||A|| \times ||x||$
### Số điều kiện của ma trận
>[!formula] Số điều kiện của ma trận
>Với ma trận không suy biến
>$$\mathrm{cond}(A) = \kappa_p(A) = ||A||\times ||A^{-1}||$$
>Với ma trận suy biến, quy ước $\mathrm{cond}(A) = \infty$

- Đặc trưng cho mức độ suy biến của ma trận:
	- Số điều kiện càng lớn, ma trận càng suy biến, khiến hệ phương trình _xác định tồi_
	- Số điều kiện càng gần 1, ma trận càng xa với suy biến, khiến hệ phương trình _xác định tốt_
- Tính chất của số điều kiện:
	- $\mathrm{cond}(A) \ge 1 \forall A$
	- $\mathrm{cond}(I) = 1$
	- $\mathrm{cond}(P) = 1$ với $P$ là ma trận hoán vị
	- $\mathrm{cond}(\alpha A) = \mathrm{cond}(A)$
	- Với $D = \mathrm{diag}(d_i)$ là ma trận đường chéo
### Đánh giá sai số dựa trên số điều kiện
- Gọi $x$ là nghiệm của $Ax=b$, $x^\star$ là nghiệm của $Ax = b + \Delta b$. $\Delta x = x^\star - x$, ta có
$$\frac{||\Delta x||}{||x||}\le \mathrm{cond}(A)\frac{||\Delta b||}{||b||}$$
- Như vậy, sự thay đổi trong lời giải $x$ khi ma trận vế phải $b$ thay đổi phụ thuộc vào số điều kiện.
- Nếu $b$ được biểu diễn gần đúng theo độ chính xác máy tính, sai số tương đối của lời giải
$$\frac{||\Delta x||}{||x||}\approx \mathrm{cond}(A)\epsilon_M$$
- Khi này lời giải thu được sẽ mất đi $\log_{10}(\mathrm{cond}(A))$ chữ số thập phân so với lời giải chính xác.