---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 8
unit: 1
title: Quy hoạch tuyến tính
---
# Quy hoạch tuyến tính
## Phát biểu bài toán
Bài toán quy hoạch tuyến tính (QHTT) làm việc với một bộ $n$ biến $(x_1; x_2;...;x_n)$, thỏa mãn một hệ $m$ phương trình/bất phương trình, với vế trái là tổ hợp tuyến tính của các biến đó, gọi là các **ràng buộc**. Mục tiêu của bài toán QHTT là tìm giá trị nhỏ nhất/ lớn nhất của một tổ hợp tuyến tính khác của các biến, gọi là **hàm mục tiêu**. 

Bài toán QHTT dạng tổng quát được phát biểu dưới dạng sau:
$$
\begin{array}{l}
f(x_1;x_2;...;x_n) = \sum_{j=1}^n{c_j x_j} \to \min/\max \\
\sum_{j=1}^n{a_{ij}x_j} = b_i \forall 1 \le i \le p \le m \\
\sum_{j=1}^n{a_{ij}x_j} = b_i \forall p < i \le m \\
x_j \ge 0 \forall 1 \le j \le q \le n \\
x_j <> 0 \forall q < j \le n (\text{ không có ràng buộc về dấu})
\end{array}
$$

Bài toán QHTT dạng chuẩn được phát biểu dưới dạng sau:
$$
\begin{array}{l}
f(x_1;x_2;...;x_n) = \sum_{j=1}^n{c_j x_j} \to \min \\
\sum_{j=1}^n{a_{ij}x_j} \ge b_i \forall 1 \le i \le m \\
x_j \ge 0 \forall 1 \le j  \le n \\
\end{array}
$$
Bài toán QHTT dạng chính tắc được phát biểu dưới dạng sau:
$$
\begin{array}{l}
f(x_1;x_2;...;x_n) = \sum_{j=1}^n{c_j x_j} \to \min \\
\sum_{j=1}^n{a_{ij}x_j} = b_i \forall 1 \le i \le m \\
x_j \ge 0 \forall 1 \le j  \le n \\
\end{array}
$$
Gọi $A$ là ma trận các hệ số $a_{ij}$ trong các ràng buộc, $\bf{b}$ ma trận cột chứa các giá trị $b_i$ trong các ràng buộc, $\bf{c}$ là ma trận hàng chứa các hệ số $c_j$ của hàm mục tiêu, $x$ là ma trận cột chứa các biến, ta có thể biểu diễn bài toán QHTT dạng chính tác dưới dạng ma trận như sau:
$$
\begin{array}{c}
\mathbf{c}x \to \min \\
Ax = \mathbf{b} \\
\mathbf{x} \ge 0
\end{array}
$$

## Đưa bài toán QHTT dạng tổng quát về dạng chính tắc

Mọi bài toán QHTT dạng tổng quát đều có thể được đưa về dạng chính tắc

[todo]

## Thuật toán đơn hình giải bài toán QHTT dạng chính tắc
Dựa trên nhận xét rằng, bài toán QHTT trong mặt phẳng luôn có nghiệm là đỉnh của miền ràng buộc, thuật toán đơn hình sẽ di chuyển từ một đỉnh ban đầu đến đỉnh kề với nó nhưng có giá trị hàm mục tiêu nhỏ hơn. Thuật toán kết thúc khi không thể tìm được đỉnh tối ưu tiếp theo, hoặc chỉ ra được hàm mục tiêu không có cận dưới.
Giả sử $\mathrm{rank}(A)=m$, tương đương với hệ $Ax = \mathbf{b}$ có nghiệm.

### Phương án cơ sở chấp nhận được
Xét một tập hợp $J_B = \{j_1; j_2;...;j_m\}$ sao cho các cột của $A$ tại các chỉ số đó là độc lập tuyến tính. Các cột này tạo thành một **cơ sở** $B$. Đặt $J_N = (1;n)\setminus J_B$.
Tính vector $B^{-1}\mathbf{b}$. Đặt các phần tử ở các chỉ số thuộc $J_N$ của vector đó bằng $0$, ta được một vector $\mathbf{x}$. $\mathbf{x}$ được gọi là một **phương án cơ sở** tương ứng với cơ sở $B$. Nếu $\mathbf{x} \ge 0$, nó được gọi là **phương án cơ sở chấp nhận được**.

