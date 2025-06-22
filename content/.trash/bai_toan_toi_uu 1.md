---
aliases: 
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 4
unit: 6
title: bai_toan_toi_uu
share: true
---
## Phát biểu bài toán
- Giả sử ta có tập $D = A_1 \times A_2 \times ... \times A_n$
- Xét một phần tử $x = (x_1; x_2; ... x_n) \in D$ và một hàm $f$
- Bài toán tối ưu yêu cầu tìm giá trị nhỏ nhất/lớn nhất của $f(x)$ với $x \in D$
- Việc này có thể đạt được bằng phương pháp duyệt toàn bộ sử dụng [[thuat_toan_quay_lui|thuật toán quay lui]], tuy nhiên để duyệt toàn bộ sẽ cần một khoảng thời gian và tài nguyên lớn.
## Thuật toán nhánh cận
- Thuật toán nhánh cận giúp giảm bớt độ phức tạp của thuật toán quay lui, bằng cách _cắt bỏ_ các nhánh nếu không đủ điều kiện
- Xét bài toán tìm giá trị nhỏ nhất của hàm $f$.
- Đầu tiên, ta xây dựng hàm $g$ thỏa mãn tính chất: với mỗi k, bất đẳng thức sau được thỏa mãn
$$g(x_1;x_2;...;x_k)\le f(x_1;x_2;...;x_n) \forall x = (x_1; x_2;...;x_n) \in D$$
- Hàm này được gọi là _hàm cận dưới_ của $f$.
- Giả sử phương án tốt nhất hiện tại là $\bar{x}$  và $f(\bar{x}) = F$. Nếu $g(x_1;x_2;...;x_k) > F$, khi đó chắc chắn $f(x) > F$, nên $x$ sẽ không thể là phương án tốt hơn $\bar{x}$. Khi đó ta sẽ dừng việc duyệt tiếp đến phương án bộ phận $k+1$, chuyển sang ứng cử viên khác cho $x_k$, và nếu không còn ứng cử viên phù hợp, ta trở về $x_{k-1}$,...
- Đối với bài toán tìm giá trị lớn nhất, ta xét _hàm cận trên_, tức là 
$$g(x_1;x_2;...;x_k)\ge f(x_1;x_2;...;x_n) \forall x = (x_1; x_2;...;x_n) \in D$$
- Và kiểm tra nếu $g < F$ thì sẽ kết thúc
- Như vậy có thể thấy, có hai yếu tố quan trọng đối với thuật toán nhánh cận:
	- Hàm cận trên/dưới
	- Tập ứng cử viên và cách duyệt
## Mã giả
- Dựa trên mã giả của thuật toán quay lui, ta bổ sung phần kiểm tra hàm cận dưới
```
Try(k):
	Xây dựng S_k;
	Với mỗi x_k trong S_k:
		Chọn x_k;
		Nếu k == n:
			Nếu f(x) < f_best:
				Cập nhật kỉ lục;
		Nếu k < n:
			Nếu g(x) <= f_best:
				Try(k+1);
		Bỏ chọn x_k;
```
- Đầu tiên ta khởi tạo `f_best = inf` hoặc một giá trị nào đó ta biết chắc lớn hơn tất cả các $f(x)$. Sau khi chạy `Try(1)`, ta sẽ có cấu hình tối ưu cần thiết.

## Một số bài toán cụ thể
### Bài toán cái túi (Knapsack Problem)
#### Phát biểu bài toán
- Giả sử ta có một cái túi có khối lượng tối đa có thể chứa được là $W$.
- Ta có $n$ món đồ, món đồ thứ $i$ có khối lượng $w_i$ và giá trị $c_i$.
- Giả sử số lượng mỗi món đồ là không hạn chế
- Bài toán: cần lấy những món đồ gì, số lượng bao nhiêu để giá trị thu được là lớn nhất?
#### Biểu diễn bài toán
- Ta có thể biểu diễn lại bài toán thành bài toán: tìm nghiệm của bất phương trình $x_1w_1 + w_2w2 + ... + w_nw_n \le W$ sao cho $x_1c_1 + x_2c_2 + ... + x_nc_n$ là lớn nhất?
- Ta sẽ sắp xếp các đồ vật theo thứ tự giảm dần về tỉ lệ giá trị/ khối lượng, tức là $\frac{c_1}{w_1} \ge \frac{c_2}{w_2} \ge ... \ge \frac{c_n}{w_n}$
- Hàm 

$$f(x_1;x_2;...;x_n) = \sum_{i=1}^{k}{x_ic_i}$$

#### Tìm hàm cận trên
- Để có thể giải bài toán trên sử dụng thuật toán nhánh cận, ta cần xác định hàm cận trên phù hợp
- Giả sử ta đã có phương án bộ phận thứ $k-1$ là $(x_1; x_2;...;x_{k-1})$. Khối lượng còn lại cái túi có thể nhận là

$$\omega_{k-1} = W - \sum_{i=1}^{k-1}{x_iw_i}$$

- Giá trị hiện tại ta đang có

$$\sigma_{k-1} = \sum_{i=1}^{k-1}{x_ic_i}$$

- Ta cần xây dựng hàm $g(x_1;x_2;...;x_k)$ sao cho $g(x_1;x_2;...;x_k) \ge f(x_1; x_2;...;x_n)$ 
- Ta có

$$f(x_1;x_2;...;x_n) = \sigma_{k-1} + \sum_{i=k}^n{x_ic_i}$$

- Theo cách sắp xếp, ta luôn có $\frac{c_i}{w_i} \le \frac{c_k}{w_k} \forall n> i > k \Rightarrow c_i \le w_i\frac{c_k}{w_k}$

$$\sum_{i=k}^n{x_ici} \le \sum_{i=k}^n{x_i w_i \frac{c_k}{w_k}} = \frac{c_k}{w_k}\sum_{i=k}^n{x_iw_i}\le\frac{c_k}{w_k}\omega_{k-1}$$

- Vậy ta có thể lấy 

$$g(x_1;x_2;...;x_k) = \sigma_{k-1} + \omega_{k-1}\frac{c_k}{w_k}$$

- Trong quá trình duyệt, ta sẽ lấy $x_i$ giảm dần từ $\lfloor\frac{\omega_{k-1}}{w_k}\rfloor$ về 0

### Bài toán người du lịch (Travelling Salesman Problem)
#### Phát biểu bài toán
- Một người du lịch muốn đi tham quan $n$ thành phố $T_1, T_2,...T_n$. 
- Xuất phát từ thành phố nào đó, người du lịch muốn đi qua tất cả các thành phố còn lại, mỗi thành phố đúng một lần, quay trở lại điểm xuất phát
- Chi phí di chuyển giữa các thành phố được biểu diễn trong ma trận $[c_{ij}]$, với $c_{ij}$ biểu thị chi phí đi từ $T_i$ đến $T_j$
- Ta cần tìm đường đi thỏa mãn yêu cầu, sao cho chi phí là thấp nhất
#### Biểu diễn bài toán
- Xét một hoán vị $x=(x_1; x_2;...x_n)$ của n số tự nhiên đầu tiên
- Chi phí di chuyển là 

$$f(x) = c_{x_1x_2} + c_{x_2x_3} + ... + c_{x_nx_1}$$
- Ta cần tìm $\min f$ 
#### Tìm hàm cận dưới
- Gọi $c_{min}$ là chi phí nhỏ nhất giữa hai thành phố bất kì
- Giả sử tại phương án bộ phận cấp $k$, ta có đường đi $x_1;x_2;...;x_{k-1};x_k$, với chi phí hiện tại là $\sigma$
- Ta còn cần phải đi $n-k+1$ đoạn đường nữa, nên ta có

$$g(x_1;x_2;...x_k) = \sigma + (n-k+1)c_{min}$$

- Ta có thể duyệt theo cách tương tự việc duyệt toán bộ để sinh hoán vị