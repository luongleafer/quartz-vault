---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 4
unit: 2
title: Thực hiện hệ thống trên miền Z
---
# Thực hiện hệ thống trên miền Z
## Hàm truyền đạt

Giả sử ta có [[xlth_he_thong_roi_rac|hệ thống]] với đáp ứng xung $h(n)$. Khi đó, với đầu vào $x(n)$, đáp ứng $y(n)$ của hệ thống là tổng chập của $x(n)$ và $h(n)$:

$$y(n) = x(n) * h(n)$$
Qua biến đổi Z, phương trình trên trở thành
$$Y(z) = X(z) H(z)$$
$H(z)$ được gọi là **hàm truyền đạt** của hệ thống.
$$H(z) = \frac{Y(z)}{X(z)}$$
Xét một hệ thống được biểu diễn bằng phương trình sai phân
$$\sum_{k=0}^N a_ky(n-k) = \sum_{k=0}^M b_k x(n-k)$$
Qua biến đổi Z, hàm truyền đạt của hệ thống có thể được xác định dưới dạng:
$$H(z) = \frac{\sum_{k=0}^M b_kz^{-k}}{\sum_{k=0}^N a_k z^{-k}}$$
Nghiệm của đa thức trên tử được gọi là các **điểm không (zeroes)**, nghiệm của đa thức dưới mẫu được gọi là **điểm cực (poles)**, kí hiệu $z_k$ là các điểm không, $p_k$ là các điểm cực, $H(z)$ có thể được biểu diễn lại dưới dạng
$$
H(z) = H_0\frac{\prod_{k=1}^M(z-z_k)}{\prod_{k=1}^N{(z-p_k)}}
$$
## Tính nhân quả của hệ thống
Giả sử $H(z)$ có miền hội tụ là $R_{h-} < |z| < R_{h+}$, trong đó $R_{x+} = \frac{1}{\lim_{n\to \infty}|x(-n)|^\frac{1}{n}}$

Hệ thống là nhân quả nếu $h(n) = 0 \forall n<0$, khi đó $R_{x+} \to \infty$. Như vậy các hệ thống với miền hội tụ của $H(z)$ có dạng $R_{h-} < |z|$ là hệ thống nhân quả.

## Tính ổn định của hệ thống
Một hệ thống được gọi là ổn định nếu $\sum_{n=-\infty}^\infty h(n) < \infty$. Khi đó, xét $|H(z)|$
$$|H(z)| = \Bigg|\sum_{n=-\infty}^\infty h(n)z^{-n}\Bigg| \le \sum_{n=-\infty}^\infty |h(n)z^{-n}|$$
Xét các điểm $z$ nằm trên đường tròn đơn vị, $|z| = 1$, khi đó $H(z)$ là hữu hạn. Vậy nếu một hệ thống là ổn định, miền hội tụ của biến đổi Z sẽ chứa đường tròn đơn vị. Điều ngược lại cũng đúng. 
Nếu hàm truyền đạt có thể được biểu diễn dưới dạng thương của hai đa thức, thì khi đó các điểm cực phải _nằm trong_ đường tròn đơn vị. 