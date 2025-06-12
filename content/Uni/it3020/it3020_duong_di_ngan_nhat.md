---
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 5
unit: 11
title: Bài toán tìm đường đi ngắn nhất
---
## Phát biểu bài toán
- Xét đồ thị có hướng $G = (V,E)$ với trọng số $c(e)$
- Đồ thị $G$ không có chu trình âm, tức là không tồn tại chu trình sao cho tổng trọng số các cạnh trong chu trình đó $\le 0$
- **Độ dài** của đường đi là tổng trọng số của các cạnh trên đường đi đó
- Xét hai đỉnh $(u;v)$ bất kì, ta cần tìm đường đi ngắn nhất giữa chúng.
- Có nhiều loại bài toán tìm đường đi ngắn nhất:
	- Giữa một cặp đỉnh $(u;v)$
	- Từ một đỉnh nguồn $s$, tìm đường đi ngắn nhất đến tất cả các đỉnh còn lại
	- Tìm đường đi ngắn nhất từ các đỉnh đến đỉnh đích $t$
	- Tìm đường đi ngắn nhất giữa mọi cặp đỉnh của đồ thị
- Để xây dựng các thuật toán tìm đường đi ngắn nhất, ta xét tính chất sau, gọi hàm $d(u;v)$ là đường đi ngắn nhất từ đỉnh $u$ đến đỉnh $v$. Giả sử ta đã tìm được giá trị $d'$, nếu tồn tại đỉnh $k$ sao cho $d(u;k) + c(k;d) < d'$, ta cập nhật $d(u;v) = d(u;k) + c(k;v)$.
## Thuật toán Bellman-Ford
- Thuật toán Bellman-Ford có thể được dùng trên đồ thị có hướng với trọng số có thể âm (nhưng không tồn tại chu trình âm). Sau khi kết thúc thuật toán, ta sẽ có được đường đi ngắn nhất từ một đỉnh $s$ đến mọi đỉnh còn lại của đồ thị.
- Khởi tạo:
	- $d[u]$ là một mảng chứa độ dài đường đi ngắn nhất giữa hai cạnh $s$ và $u$. Ban đầu $d[s] = 0$ và $d[u] = \infty$ với mọi đỉnh $u$, do chưa tìm được đường đi nào giữa $s$ và $u$
	- $p[u]$ là mảng chứa đỉnh liền trước $u$ trong đường đi ngắn nhất giữa $s$ và $u$. Ví dụ, nếu đường đi đó là $s\rightarrow a \rightarrow b \rightarrow u$ thì $p[u] = b$. Khởi tạo $p[u] = \mathrm{NULL}$ với mọi đỉnh $u$  
- Thuật toán Bellman-Ford thực hiện $n-1$ vòng lặp ($n$ là số đỉnh của đồ thị), trong mỗi vòng lặp:
	- Duyệt toàn bộ cạnh $(u;v) \in E$ với trọng số $w$
	- Với mỗi cạnh $(u;v)$, nếu $d[u] + w < d[v]$:
		- cập nhật $d[v] = d[u] + w$
		- cập nhật $p[v] = u$
- Thuật toán có thể kết thúc sớm nếu trong toàn bộ quá trình duyệt cạnh, không có cập nhật nào được thực hiện.
- Độ phức tạp của thuật toán:
	- Về thời gian chạy:
		- Trường hợp tốt nhất $\Theta(|E|)$
		- Trường hợp xấu nhất $\Theta(|V||E|)$
	- Về tài nguyên $\Theta(|V|)$

## Thuật toán Dijkstra
- Được sử dụng trên đồ thị với trọng số không âm
- Sau khi kết thúc thuật toán, ta thu được đường đi ngắn nhất từ đỉnh $s$ đến mọi đỉnh còn lại của đồ thị
- Khởi tạo:
	- $d[u]$ là mảng chứa độ dài đường đi ngắn nhất giữa $s$ và $u$. Đặt $d[s] = 0$, $d[u] = c(s;u)$ nếu $(s;u) \in E$ và $d[u] = \infty$ nếu ngược lại
	- $p[u]$ là mảng chứa đỉnh liền trước $u$ trong đường đi ngắn nhất giữa $s$ và $u$
	- Gán nhãn đỉnh $s$ là "đã thăm"
- Thuật toán Dijkstra lặp cho đến khi tất cả các đỉnh đều được gán nhãn "đã thăm", trong mỗi vòng lặp, thực hiện thao tác sau:
	- Trong các đỉnh chưa được gán nhãn, tìm $u$ là đỉnh có $d[u]$ nhỏ nhất.
	- Gán nhãn đỉnh $u$ là "đã thăm"
	- Xét các đỉnh $v$ kề với $u$, nếu $d[u] + c(u;v) < d[v]$:
		- cập nhật $d[v] = d[u] + c(u;v)$
		- cập nhật $p[v] = u$
- Độ phức tạp của thuật toán Dijkstra là $\Theta(|V|^2)$, tuy nhiên điều này có thể được cải thiện đối với đồ thị thưa và sử dụng các cấu trúc dữ liệu phù hợp

## Đối với đồ thị không có chu trình
- Trong một đồ thị không có chu trình, ta luôn có thể đánh số các đỉnh, sao cho mỗi cung chỉ đi từ đỉnh số nhỏ đến đỉnh số lớn hơn.
- Một thuật toán đánh số đỉnh có thể được miêu tả như sau:
	- Tìm các đỉnh có bán bậc vào bằng 0, do đồ thị không có chu trình nên chắc chắn có đỉnh này. Đánh số các đỉnh theo thứ tự tùy ý
	- Loại bỏ các đỉnh vừa đánh số và các cạnh kề với nó.
	- Lặp lại 2 bước trên cho đến khi tất cả các đỉnh đã được đánh số
- Độ phức tạp của thuật toán đánh số trên là $\Theta(|V|)$
- Sau khi đã đánh số, ta có thể duyệt các đỉnh theo thứ tự đánh số, thực hiện việc cập nhật tương tự như trên. 
- Khi này, độ phức tạp của thuật toán tìm đường đi ngắn nhất là $\Theta(|V|)$, do ta chỉ duyệt các cạnh đúng 1 lần

## Thuật toán Floyd-Warshall
- Có thể sử dụng trên đồ thị có trọng số có thể âm
- Sau khi kết thúc thuật toán, ta thu được đường đi ngắn nhất giữa mọi cặp đỉnh của đồ thị
- Giả sử các đỉnh được đánh số từ $1$ đến $n$
- Khởi tạo
	- $D = [d_{uv}]$ là ma trận lưu đường đi ngắn nhất giữa hai đỉnh $u$ và $v$. $d_{uv} = c(u;v)$ nếu $(u;v) \in E$
	- $P = [p_{uv}]$ lưu đỉnh liền trước $v$ trong đường đi ngắn nhất giữa $u$ và $v$. $p_{uv} = u$ nếu $(u;v) \in E$
- Gọi $D(k)$ và $P(k)$ là ma trận đường đi ngắn nhất và đỉnh liền trước, sử dụng $k$ đỉnh đầu tiên của đồ thị. $D = D(n)$, $P=P(n)$
- Thuật toán Floyd-Warshall xây dựng $D(k)$ và $P(k)$ với $k$ từ $1$ đến $n$. $D(0)$ và $P(0)$ là ma trận có được sau bước "khởi tạo"
- Với mỗi $k$, nếu $d^{(k-1)}_{uv} > d^{(k-1)}_{uk} + d^{(k-1)}_{kv}$
	- $d^{(k)}_{uv} = d^{(k-1)}_{uk} + d^{(k-1)}_{kv}$
	- $p^{(k)}_{uv} = p^{(k-1)}_{kv}$
