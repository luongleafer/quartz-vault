---
aliases: 
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 5
unit: 10
title: it3020_cay_khung_nho_nhat
share: true
---
## Cây
>[!definition] Định nghĩa
>**Cây** là một đồ thị vô hướng liên thông, không có chu trình đơn.
>**Rừng** là đồ thị không có chu trình. Các thành phần liên thông của rừng là cây.

- Các tính chất của cây:
	- Cây có $n$ đỉnh thì có $n-1$ cạnh
	- Mỗi cạnh của cây đều là cầu
	- Hai đỉnh bất kì của cây được nối với nhau bằng một và chỉ một đường đi đơn
	- Khi thêm bất kì một cạnh nào, ta thu được một chu trình
- Cho đồ thị $G=(V,E)$ vô hướng, liên thông. Cây $T=(V,F)$ với $F\subseteq E$ được gọi là **cây khung** của đồ thị $G$

>[!formula] [Công thức Cayley](https://en.wikipedia.org/wiki/Cayley%27s_formula)
>Số cây khung của đồ thị $n$ đỉnh là $n^{n-2}$

## Bài toán cây khung nhỏ nhất
- Xét đồ thị vô hướng có trọng số $G = (V,E)$, trong đó trọng số cạnh $e$ được kí hiệu là $c(e)$. Ta cần tìm cây khung có tổng trọng số các cạnh là nhỏ nhất

### Thuật toán Kruskal
- Xét $T = \emptyset$
- Sắp xếp tập cạnh $E$ theo thứ tự tăng dần của trọng số
- Với mỗi cạnh trong $E$, từ trọng số nhỏ đến lớn, bổ sung vào $T$ sao cho việc bổ sung không tạo thành chu trình
- Thuật toán kết thúc khi đã duyệt hết cạnh trong $E$ hoặc $T$ có $n-1$ cạnh
- Độ phức tạp: $O(m\log m)$ với $m$ là số cạnh của đồ thị
- Thuật toán Kruskal thường được dùng cho các đồ thị thưa
### Thuật toán Prim
- Xét $T = {s}$, với $s$ là một đỉnh bất kì của đồ thị 
- Chọn cạnh $e$ sao cho $e$ là cạnh nhỏ nhất giữa một đỉnh trong tập $T$ và một đỉnh ngoài tập $T$ mà khi bổ sung vào $T$ không tạo ra chu trình
- Bổ sung cạnh $e$ vào T
- Thuật toán được lặp lại cho đến khi $T$ có đủ $n$ đỉnh và $n-1$ cạnh
- Độ phức tạp: $O(m\log n)$ với $m$ là số cạnh, $n$ là số đỉnh, thực hiện trên danh sách kề và đống nhị phân (binary heap)
