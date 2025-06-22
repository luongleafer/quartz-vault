---
aliases: 
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 5
unit: 12
title: it3020_luong_cuc_dai
share: true
---
## Mạng và luồng

>[!definition] Mạng và khả năng thông qua
>**Mạng (network)** là đồ thị có hướng có đúng 1 đỉnh có bán bậc vào bằng 0, gọi là **đỉnh nguồn (source)**, và đúng 1 đỉnh có bán bậc ra bằng 0, gọi là **đỉnh đích (sink)**.
>Trên mỗi cung $e$ của mạng, định nghĩa $c(e)$ là **khả năng thông qua (capacity)** của cung $e$

- $c(e) \ge 0$ với mọi $e$ trong mạng. Quy ước $c(u;v) = 0$ nếu $(u;v) \notin E$

>[!definition] Luồng
>**Luồng (flow)** là một ánh xạ $f: E \to \{x | x \in \mathbb{R}, x \ge 0\}; e \mapsto f(e)$
>thỏa mãn các điều kiện dưới đây

- (1) Luồng không vượt quá khả năng thông qua, tức là
$$f(e) \le c(e)$$
- (2) Điều kiện cân bằng đỉnh, với mỗi $u$, trừ đỉnh nguồn và đỉnh đích, tổng luồng trên các cung đi vào $u$ bằng tổng luồng trên các cung đi ra khỏi $u$
$$\sum_{(k;u) \in E}f(k;u) = \sum_{(u;k)\in E}f(u;k)$$
Từ điều kiện (2), gọi $s$ là đỉnh nguồn và $t$ là đỉnh đích, ta có
$$\sum_{(s;u)\in E}f(s;u) = \sum_{(u;t)\in E}f(u;t) = v$$
Giá trị $v$ được gọi là **giá trị của luồng**, kí hiệu $v = \mathrm{val}(f)$

## Bài toán tìm luồng cực đại
- Trong số các luồng trên mạng $G = (V,E)$ , ta cần tìm luồng có giá trị lớn nhất.
>[!definition] Lát cắt
>**Lát cắt** là một phân hoạch $(S,T)$ của tập đỉnh V sao cho $s \in S$ và $t \in T$
>Khả năng thông qua của lát cắt là tổng khả năng thông qua của các cung đi từ một đỉnh thuộc $S$ đến một đỉnh thuộc $T$

- **Lát cắt hẹp nhất** là lát cắt có khả năng thông qua nhỏ nhất. Giá trị nhỏ nhất này cũng là giá trị của luồng cực đại. Nói cách khác, giá trị của mọi luồng trong mạng đều không vượt quá khả năng thông qua của lát cắt hẹp nhất
## Thuật toán Fold-Fulkerson
### Đồ thị dư và đường tăng luồng
- Xét mạng $G(V,E)$ có khả năng thông qua trên cạnh $(u;v) \in E$ là $c(u;v)$.
- Xét luồng $f$ trên $G$.
- Xây dựng đồ thị $G_f = (V, E_f)$ :
	- Với mỗi cạnh $(u;v) \in E$, thêm cạnh $(u;v)$ vào  $E_f$ có trọng số là $c(u;v) - f(u;v)$ và cạnh $(v;u)$ có trọng số $f(u;v)$
	- Loại bỏ các cạnh có trọng số bằng 0
- Đồ thị $G_f$ được gọi là **đồ thị tăng luồng** hoặc **đồ thị dư (residual graph)**
- Nhận xét: nếu $f$ không phải luồng cực đại, ta luôn tìm được đường đi từ $s$ đến $t$ trong $G_f$. Đường này được gọi là **đường tăng luồng**

### Mô tả thuật toán
- Bước 1: Xây dựng luồng $f$ có $f(e) = 0$ với mọi $e \in E$. Xây dựng $G_f$ tương ứng
- Bước 2: Tìm đường đi $P$ từ $s$ đến $t$ trong $G_f$. Nếu không có, kết thúc thuật toán
- Bước 3: Đặt $\theta$ là trọng số nhỏ nhất của cung trong đường đi vừa tìm được ở Bước 2
- Bước 4: Cập nhật $f$:
	- $f(u;v) = f(u;v) + \theta$ nếu $(u;v) \in P$
	- $f(u;v) = f(u;v) - \theta$ nếu $(v;u) \notin P$
- Bước 5: Cập nhật $G_f$ và lặp lại bước 2

### Thuật toán Edmonds-Karp
- Việc tìm đường tăng luồng ở Bước 2 quyết định đến độ hiệu quả của thuật toán
- Trong thuật toán Edmonds-Karp, ở bước 2, ta thực hiện [[duyet_do_thi#Phương pháp duyệt theo chiều rộng (Breadth-First Search - BFS)|duyệt theo chiều rộng]]
