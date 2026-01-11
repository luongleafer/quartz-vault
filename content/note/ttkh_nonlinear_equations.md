---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 4
unit: 4
title: Giải phương trình phi tuyến
---
# Giải phương trình phi tuyến
## Vấn đề
- Xét hàm $f(x)$ là hàm phi tuyến tính (non-linear function), ta cần tìm nghiệm của phương trình
$$f(x) = 0$$
- Nghiệm của phương trình trên còn được gọi là **không điểm** của hàm $f(x)$. Kí hiệu nghiệm đúng của phương trình là $x\star$
- Việc tìm nghiệm được gọi là **bài toán tìm nghiệm (root finding)**.
- Do $f(x)$ phi tuyến, nghiệm thường không có công thức tường minh để tìm kiếm.
- Khi này ta sử dụng phương pháp lặp để tìm giá trị _gần đúng_ của nghiệm, trong khoảng sai số cho phép $\epsilon$
- Phương pháp chủ yếu là lặp liên tiếp tính giá trị $x_k$ dựa trên một/một số giá trị đã tính từ trước. 
- Việc lặp dừng lại khi $|f(x_k)| < \epsilon$ hoặc $|x\star -x_k|<\epsilon$
- Gọi sai số tại bước lặp thứ $k$ là $e_k = x_k - x\star$, nếu
$$\lim_{k\to \infty}\frac{|e_{k+1}|}{|e_k|^r} = C (const,\neq 0)$$
ta gọi dãy ${e_k}$ hội tụ cấp $r$ 
- Đoạn $[a;b]$ được gọi là **khoảng phân ly nghiệm** của hàm $f$ nếu $f(a)f(b)<0$. Nếu $f$ liên tục, trên đoạn này chắc chắn tồn tại nghiệm.
## Các phương pháp tìm nghiệm
### Phương pháp chia đôi
- Xét khoảng phân li nghiệm ban đầu $[a;c]$, giả thiết chỉ có một nghiệm
- Đặt $$b = \frac{a+c}{2}$$
- $b$ là hoành độ trung điểm của $(a;0)$ và $(c;0)$
- Tính $f(b)$:
	- Nếu bằng 0, kết luận $b$ là nghiệm
	- Nếu $f(a)f(b) < 0$, lặp lại với khoảng phân li nghiệm $[a;b]$
	- Nếu $f(b)f(c) <0$, lặp lại với khoảng phân li nghiệm $[b;c]$
- Điều kiện dừng: $|c-a|  < \epsilon$

### Phương pháp dây cung
- Xét khoảng phân li nghiệm ban đầu $[a;c]$, giả thiết chỉ có một nghiệm
- Đặt
$$b = a - \frac{c-a}{f(c)-f(a)}f(a)$$
- $b$ là hoành độ của giao giữa đường thẳng AC với trục hoành, với $A(a;f(a))$ và $C(c;f(c))$
- Xét $f(b)$ tương tự như phương pháp chia đôi

### Phương pháp Newton
- Xét điểm xấp xỉ ban đầu $x_0$
- [[Ch1_B04_Định_lí_hàm_khả_vi#Khai triển Taylor (hữu hạn)|Khai triển Taylor]] đến cấp 2 của hàm $f(x)$ tại điểm $x_0$
$$f(x) = f(x_0) + f'(x_0)(x-x_0)+o((x-x_0)^2)$$
- Dựa trên công thức này, $x$ có thể được tính xấp xỉ theo công thức
$$x = x_0 - \frac{f(x_0)}{f'(x_0)}$$
- Từ $x_0$ ban đầu, giá trị $x$ sẽ gần nghiệm đúng $x\star$ hơn, lặp lại cho đến khi $|f(x_k)| < \epsilon$
- Khi này, $x_{k+1}$ sẽ là hoành độ của giao điểm giữa tiếp tuyến của đồ thị hàm $f(x)$ tại điểm $(x_k;f(x_k))$

### Phương pháp cát tuyến
- Xét hai điểm xấp xỉ ban đầu $x_0$ và $x_1$
- Với $k \ge 2$, đặt
$$s_k = \frac{f(x_k) - f(x_{k-1})}{x_k - x_{k-1}}$$
$$x_{k+1} = x_k - \frac{f(x_k)}{s_k}$$
- Lặp cho đến khi $|f(x_k) < \epsilon|$
- Khi này, $x_{k+1}$ là hoành độ giao điểm giữa đường thẳng đi qua $(x_k;f(x_k))$ và $(x_{k-1};f(x_{k-1}))$

### Phương pháp lặp
- Đưa việc giải $f(x) = 0$ về dạng tìm $x$ để $x = g(x)$ với $g(x)$ là một hàm do ta xác định dựa trên $f(x)$
- Đối với phương pháp Newton, $g(x) = x - \frac{f(x)}{f'(x)}$
- Từ giá trị xấp xỉ $x_0$ ban đầu, lặp cho đến khi $|x_k - g(x_k)| < \epsilon$, đặt $x_k = g(x_{k-1})$

## So sánh giữa các phương pháp

| Phương pháp | Cần khoảng phân li nghiệm? | Cần đạo hàm liên tục? | Kiểu phương trình | Điểm mạnh                                    | Điểm yếu                                                               |
| ----------- | -------------------------- | --------------------- | ----------------- | -------------------------------------------- | ---------------------------------------------------------------------- |
| Chia đôi    | Có                         | Không                 | Bất kỳ            | Có thể xử lí các hàm không có dạng giải tích | - Không xét được nghiệm kép<br>- Không xử lí được điểm kì dị           |
| Dây cung    | Có                         | Không                 | Bất kỳ            | Như trên                                     | - Hội tụ chậm                                                          |
| Newton      | Không                      | Có                    | Bất kỳ            | Hội tụ bình phương                           | - Không phải lúc nào cũng hội tụ<br>- Không thể tính đạo hàm chính xác |
| Cát tuyến   | Không                      | Có                    | Bất kỳ            |                                              | Hội tụ trên tuyến tính                                                 |
| Lặp         | Không                      | Có                    | Bất kỳ            |                                              | Không phải lúc nào cũng hội tụ                                         |
