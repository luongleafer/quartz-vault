---
aliases: 
subject: "[[it3020]]"
tags:
  - university
  - note
chapter: 3
unit: 4
title: Thuật toán sinh
share: true
---

# Thuật toán sinh

## Sơ lược thuật toán
- Xác định thứ tự từ điển, cấu hình đầu và cuối
- Xác định thuật toán sinh kế tiếp
- Sinh cấu hình đầu tiên, cho đến khi chưa phải cấu hình cuối cùng, sinh cấu hình kế tiếp
## Ứng dụng
### Bài toán sinh dãy nhị phân độ dài n
- Đặt $a = a_0a_1...a_{n-1}$, với $a_i = 0 || 1$
- Gọi N là số thập phân tương ứng với xâu nhị phân $a$, N' là số thập phân tương ứng với xâu nhị phân $a'$.
- Thứ tự từ điển: $a$ trước $a'$ nếu N < N'.
- Cấu hình đầu tiên: $00...0$ ($n$ số 0)
- Cấu hình cuối cùng: $11...1$ ($n$ số 1)
- Thuật toán sinh kế tiếp:
	- Xét từ phải sang trái, tìm chữ số $k$ đầu tiên sao cho $a_k = 0$
	- $a_k \leftarrow 1$; $a_m \leftarrow 0$ với $k < m < n$
	- Ví dụ: 00110 -> 00111 -> 01000
### Bài toán sinh tổ hợp chập k của n phần tử
- Xét tập hợp n số tự nhiên đầu tiên
- Tổ hợp chập k của n phần tử có dạng $a = (a_0; a_1; ...; a_{k-1})$ với $1 \le a_i \le n; a_0 < a_1 <... <a_{k-1}$ 
- Thứ tự từ điển: $a$ trước $a'$ nếu tồn tại $m$ sao cho $a_i = a'_i \, \forall 0 \le i <m$ và $a_m < a'_m$
- Cấu hình đầu tiên: $(1;2;...;k)$
- Cấu hình cuối cùng: $(n-k+1;n-k+2;...;n)$
- Thuật toán sinh kế tiếp
	- Xét từ phải sang trái, tìm vị trí $m$ đầu tiên sao cho $a_m \neq n-k+m +1$ 
	- $a_m \leftarrow a_m + 1$; $a_i \leftarrow a_m + 1 + (i - m)$ với $m < i \le k$
	- Ví dụ với $n=6; k = 4$ $(2;3;4;5) \rightarrow (2;3;4;6) \rightarrow (2;3;5;6)$
### Bài toán sinh hoán vị của n phần tử
- Xét tập hợp n số tự nhiên đầu tiên
- Một hoán vị có dạng $a = (a_0; a_1;...;a_{n-1})$ với $1 \le a_i \le n$ và $a_i \neq a_j \forall i \neq j$
- Thứ tự từ điển: tương tự chỉnh hợp
- Cấu hình đầu tiên: $(1;2;...;n)$
- Cấu hình cuối cùng: $(n;n-1;...;1)$
- Thuật toán sinh kế tiếp
	- Tính từ phải qua trái, tìm vị trí $j$ đầu tiên sao cho $a_j < a_{j+1}$ 
	- Tìm vị trí $k>j$ sao cho $a_k$ nhỏ nhất, lớn hơn $a_j$
	- Đổi chỗ $a_j$ và $a_k$
	- Lật ngược đoạn $a_{j+1}$ đến $a_n$
	- Ví dụ: $n = 6$, $(1;2;3;4;5;6) \rightarrow (1;2;3;4;6;5) \rightarrow (1;2;3;5;4;6)$