---
aliases: 
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 3
unit: 5
title: thuat_toan_quay_lui
share: true
---
## Bài toán
- Xét tập $A = A_1 \times A_2 \times ... \times A_n$
- Gọi $P$ là một tính chất trên $A$, ta cần liệt kê tất cả các $a \in A$ thỏa mãn tính chất $P$
- $a$ có dạng $a = (a_1;a_2;...;a_n)$ với $a_i \in A_i, 1 \le i \le k$
## Thuật toán
- Xét **lời giải bộ phận cấp k** có dạng $s_k = (a_1;a_2;...;a_k)$ với $a_i \in A_i, 1\le i \le k$
	- Khi $k = 0$ ta có **lời giải rỗng**
	- Khi $k = n$ ta có **lời giải đầy đủ**
- Xét từ lời giải rỗng, ta xác định những phần tử, gọi là tập ứng cử viên $S_1$ của $A_1$ có thể chọn vào vị trí $a_1$ để đảm bảo $P$.
- Từ lời giải cấp $k-1$, ta xác định tập ứng củ viên $S_k$ có thể chọn vào vị trí $a_k$
	- Nếu $S_k = \emptyset$, quay lại lời giải cấp $k-1$, tìm ứng cử viên khác thay vào $a_{k-1}$
	- Nếu $S_k \neq \emptyset$ , bổ sung một phần tử vào lời giải.
		- Nếu $k = n$, kết thúc, trả về vời giải
		- Nếu $k < n$, tiếp tục thay lần lượt các giá trị trong $S_k$ vào $a_k$ và tiếp tục
## Mã giả
Xét hàm `Try(k)`
```
Try(k):
	Xây dựng S_k;
	Với x_k trong S_k:
		Chọn x_k;
		Nếu k == n:
			Lưu cấu hình;
		Nếu k < n:
			Try(k+1);
		Bỏ chọn x_k;
```
Để bắt đầu thuật toán sinh, ta gọi `Try(1)`