---
aliases: 
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 5
unit: 7
title: khai_niem_do_thi
share: true
---
## Định nghĩa đồ thị
- Đồ thị G là tập hợp các đỉnh $V$ và các cạnh $E \subseteq V^2$ nối giữa các đỉnh đó.
- Kí hiệu $G = (V, E)$
## Các loại đồ thị
- Đơn đồ thị: giữa hai đỉnh bất kì chỉ có _nhiều nhất một cạnh_
- Đa đồ thị: giữa hai đỉnh bất kì có thể có nhiểu hơn một cạnh
- Đồ thị vô hướng: cạnh là bộ đỉnh _không có thứ tự_
- Đồ thị có hướng: cạnh là bộ đỉnh _có thứ tự_
## Một số khái niệm trong đồ thị
### Đỉnh kề nhau
- Xét trong đồ thị vô hướng, nếu tồn tại $e = (u;v) \in E$, ta nói u và v là hai đỉnh _kề nhau_, $e$ là **cạnh nối** hai đỉnh $u$ và $v$, $u$ và $v$ là **đầu mút** của cạnh $e$
- Xét trong đồ thị có hướng, nếu tồn tại $e = (u;v) \in E$, ta gọi $u$ là **đỉnh bắt đầu**, $v$ là **đỉnh kết thúc** của $e$. $e$ _đi ra_ từ $u$ và _đi vào_ $v$
### Bậc
- Bậc của một đỉnh là số cạnh _kề_ với nó, kí hiệu $\deg(v)$
	- đỉnh có bậc bằng không được gọi là **đỉnh cô lập**
	- đỉnh có bậc bằng 1 được gọi là **đỉnh treo**
- Đối với đồ thị có hướng:
	- **bán bậc vào** của một đỉnh là số cạnh đi vào đỉnh đó, kí hiệu $\deg^-(v)$
	- **bán bậc ra** của một đỉnh là số cạnh đi ra khỏi đỉnh đó, kí hiệu $\deg^+(v)$
	- bậc của đỉnh là tổng của bán bậc vào và bán bậc ra $\deg(v) = \deg^-(v) + \deg^+(v)$
	- đỉnh có bán bậc vào bằng 0 được gọi là **đỉnh nguồn**
	- đỉnh có bán bậc ra bằng 0 được gọi là **đỉnh đích**
- Trong đơn đồ thị, Tổng bậc của tất cả các đỉnh bằng hai lần số cạnh $\sum_{v \in V}{\deg(v)} = 2 |E|$
- Số đỉnh bậc lẻ luôn là số chẵn

### Đồ thị con
- Xét $G = (V;E)$. $G'= (V';E')$ được gọi là **đồ thị con** của $G$ nếu $V' \subseteq V$ và $E' \subseteq E$
- **Đồ thị con bao trùm** là đồ thị con có tập đỉnh bằng tập đỉnh của đồ thị chứa nó
### Đồ thị đẳng cấu
- $G_1 = (V_1; E_1)$ và $G_2 = (V_2; E_2)$ được gọi là **đẳng cấu** nếu tồn tại [[Ch1_B02_Ánh_xạ#Song ánh|song ánh]] $f: V_1 \to V_2$ sao cho với mỗi $(u;v) \in E_1$ thì $(f(u); f(v)) \in E_2$
- Khi đó $G_1$ và $G_2$ là **hai đồ thị đẳng cấu**
- Điều kiện cần: hai đồ thị đẳng cấu sẽ:
	- cùng số cạnh
	- cùng số đỉnh
	- số đỉnh bậc $k$ là như nhau với mọi $k$
### Đường đi
- Xét $u; v \in V$ 
- Một **đường đi** từ $u$ đến $v$ là dãy $u; x_1; x_2;...; x_{n-1}; v$ với $x_i \in V; (u;x_1) \in E; (x_{n-1};v) \in E; (x_i;x_j) \in E$
- **Đường đi đơn** là đường đi không qua một đỉnh quá 1 lần
- Đường đi cơ bản: đường đi không qua một cạnh quá 1 lần
- Nếu tồn tại đường đi từ $u$ đến $v$, ta nói $v$ _đạt được_ từ $u$
	- Mỗi đỉnh đều đạt được từ chính nó
- **Chu trình** là đường đi có điểm đầu trùng điểm cuối
### Tính liên thông của đồ thị
- Một đồ thị vô hướng được gọi là _liên thông_ nếu luôn tồn tại đường đi giữa hai đỉnh bất kì
	- Đồ thị có hướng được gọi là _liên thông yếu_ nếu đồ thị vô hướng tương ứng với nó là đồ thị liên thông
	- Đồ thị có hướng được gọi là _liên thông mạnh_ nếu luôn tồn tại đường đi giữa hai đỉnh bất kì
- Một **thành phần liên thông** là một đồ thị con liên thông, nhưng nếu bổ sung bất kì một cạnh/đỉnh khác sẽ khiến nó không liên thông nữa
- Đỉnh mà khi bỏ nó đi, làm tăng số thành phần liên thông của đồ thị, được gọi là **đỉnh rẽ nhánh**
- Cạnh với tính chất như trên được gọi là **cầu**

### Một số đường đi đặc biệt
- Đường đi Euler là đường đi qua _mỗi cạnh đúng một lần_
- Chu trình Euler là đường đi qua _mỗi cạnh đúng một lần_, có đỉnh đầu trùng đỉnh cuối
- Đồ thị vô hướng có chu trình Euler khi và chỉ khi nó _không có đỉnh bậc lẻ_
- Đồ thị vô hướng có đường đi Euler khi và chỉ khi nó _có đúng hai đỉnh bậc lẻ_. Đó là điểm đầu và điểm cuối của đường đi
- Đường đi Halminton là đường đi qua _mỗi đỉnh đúng một lần_
- Chu trình Halminton là chu trình đi qua _mỗi đỉnh đúng một lần_, không tính điểm đầu trùng điểm cuối
- Đơn đồ thị vô hướng có số đỉnh $n \ge 3$ có chu trình Halminton nếu bậc của mỗi đỉnh không nhỏ hơn $\frac{n}{2}$
