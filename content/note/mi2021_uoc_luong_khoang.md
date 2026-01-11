---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 3
unit: 4
title: Ước lượng khoảng
---
# Ước lượng khoảng
Xét [[mi2021_tong_the_va_mau|tổng thể]] với đặc tính cần quan sát được đặc trưng bởi biến ngẫu nhiên $X$. Ta cần ước lượng tham số $\theta$ của $X$. Lập [[mi2021_mau_ngau_nhien|mẫu ngẫu nhiên]] kích thước $n$.

Để ước lượng $\theta$, ta chọn hai thống kê $\hat{\Theta}_1$ và $\hat{\Theta}_2$. Nếu $$P(\hat{\Theta}_1 \le \theta \le \hat{\Theta}_2) = \gamma$$ với $\gamma$ là một số gần 1 cho trước, ta nói:
- $(\hat{\Theta}_1; \hat{\Theta}_2)$ là _khoảng tin cậy_ cho tham số $\theta$
- $\gamma$ là _độ tin cậy_ cho ước lượng khoảng
- $\bar{\Theta}_2 - \bar{\Theta}_1$ là _độ dài khoảng tin cậy_


Một số loại khoảng tin cậy:
- Nếu ta chỉ xét cận trên, ta có **khoảng tin cậy tối đa**
- Nếu ta chỉ xét cận dưới, ta có **khoảng tin cậy tối thiểu**
- Nếu ta xét cả cận trên và dưới, ta có **khoảng tin cậy hai phía**
- Nếu khoảng tin cậy đối xứng qua [[mi2021_uoc_luong_diem|ước lượng điểm]] ta có **khoảng tin cậy đối xứng**
## Ước lượng khoảng của giá trị kỳ vọng
Xét biến ngẫu nhiên $X$ có kỳ vọng $\mu$ chưa biết. Lập mẫu ngẫu nhiên kích thước $n$ $(X_1; X_2;...;X_n)$. Ta có $\overline{X}$ là trung bình mẫu ngẫu nhiên và $S$ là phương sai mẫu ngẫu nhiên đã hiệu chỉnh. Ta cần ước lượng khoảng cho $\mu$ với độ tin cậy $1-\alpha$.

### Trường hợp $X$ có phân phối chuẩn, phương sai đã biết

Xét thống kê:
$$Z = \frac{\overline{X}-\mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0;1)$$
Gọi $z_{t}$ là giá trị sao cho $P(Y \le z_t) = 1-t$ với $Y$ là biến ngẫu nhiên có phân phối chuẩn tắc. Do tính đối xứng của đồ thị hàm mật độ xác suất phân phối chuẩn tắc, ta có $P(Y \ge -t) = 1-t$
Khi đó ta có\
$$
\begin{aligned}
P(-z_{\frac{\alpha}{2}} \le Z \le z_{\frac{\alpha}{2}}) &= 1 - \alpha \\
P(-z_{\frac{\alpha}{2}} \le \frac{\overline{X}-\mu}{\frac{\sigma}{\sqrt{n}}} \le z_{\frac{\alpha}{2}}) &= 1 - \alpha \\
P(\overline{X}-z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}\le \mu \le \overline{X}+z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}) &= 1-\alpha
\end{aligned}
$$
Lúc này ta có khoảng tin cậy đối xứng của $\mu$ với độ tin cậy $1-\alpha$ là $\big(\overline{X}-z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}} ; \overline{X}+z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}\big)$.
Với mẫu cụ thể, ta có khoảng tin cậy đối xứng của $\mu$ với độ tin cậy $1-\alpha$ là $\big(\overline{x}-z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}} ; \overline{x}+z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}\big)$
Ngoài ra, ta có nhận xét
$$P(Z \ge -z_\alpha) = 1 - \alpha \Leftrightarrow P\bigg(\mu \le \overline{X} + z_\alpha\frac{\sigma}{\sqrt{n}}\bigg) = 1 - \alpha$$
Vậy khoảng tin cậy tối đa của $\mu$ với độ tin cậy $1-\alpha$ là $\bigg(-\infty; \overline{X} + z_\alpha\frac{\sigma}{\sqrt{n}}\bigg)$
Tương tự, khoảng tin cậy tối thiểu của $\mu$ với độ tin cậy $1-\alpha$ là $\bigg(\overline{X} - z_\alpha\frac{\sigma}{\sqrt{n}}; +\infty\bigg)$

### Trường hợp $X$ có phân phối chuẩn, phương sai chưa biết

Nếu $X$ có phân phối chuẩn với phương sai $\sigma^2$ chưa biết, xét thống kê
$$T = \frac{\overline{X}- \mu}{\frac{S}{\sqrt{n}}}$$ có phân phối Student với $n-1$ bậc tự do.
Khi đó, đặt $t_{m; n-1}$ là giá trị sao cho $P(t_{m;n-1} \le Y) =  1-m$ với $Y$ là biến ngẫu nhiên có phân phối Student với $n-1$ bậc tự do, thực hiện tương tự mục trước ta thu được:
Khoảng tin cậy đối xứng của $\mu$ với độ tin cậy $1-\alpha$
$$\bigg(\overline{X} - t_{\frac{\alpha}{2};n-1}\frac{S}{\sqrt{n}}; \overline{X} + t_{\frac{\alpha}{2};n-1}\frac{S}{\sqrt{n}}\bigg)$$
Khoảng tin cậy tối đa của $\mu$ với độ tin cậy $1-\alpha$
$$\bigg(-\infty; \overline{X} + t_{\alpha;n-1}\frac{S}{\sqrt{n}}\bigg)$$
Khoảng tin cậy tối thiểu của $\mu$ với độ tin cậy $1-\alpha$
$$\bigg(\overline{X} - t_{\alpha;n-1}\frac{S}{\sqrt{n}}; +\infty\bigg)$$

## Trường hợp $X$ có phân phối bất kì, kích thước mẫu đủ lớn (thường khoảng 30)
Khi kích thước mẫu đủ lớn, trung bình mẫu ngẫu nhiên xấp xỉ phân phối chuẩn, phân phối Student xấp xỉ phân phối chuẩn. Như vậy, trong trường hợp phương sai đã biết, ta đưa về trường hợp $X$ có phân phối chuẩn. Trường hợp phương sai chưa biết, ta có:
Khoảng tin cậy đối xứng của $\mu$ với độ tin cậy $1-\alpha$
$$\big(\overline{X}-z_{\frac{\alpha}{2}}\frac{S}{\sqrt{n}} ; \overline{X}+z_{\frac{\alpha}{2}}\frac{S}{\sqrt{n}}\big)$$
Khoảng tin cậy tối đa của $\mu$ với độ tin cậy $1-\alpha$
$$\bigg(-\infty; \overline{X}+z_\alpha\frac{S}{\sqrt{n}}\bigg)$$
Khoảng tin cậy tối thiểu của $\mu$ với độ tin cậy $1-\alpha$
$$\bigg(\overline{X}-z_{\alpha}\frac{S}{\sqrt{n}}; +\infty\bigg)$$
Lưu ý: Đối với mẫu cụ thể, cần thay các giá trị của thống kê ($\overline{x}$, $s$) vào các khoảng tin cậy trên.

## Ước lượng khoảng của giá trị tỉ lệ
Xét một đặc điểm định tính $A$ nào đó trong tổng thể, với tỉ lệ cá thể có đặc tính $A$ là $p$ chưa biết. Gọi $X$ là biến ngẫu nhiên có phân phối Bernoulli, với $X=1$ biểu thị "có đặc tính A",  và $X=0$ biểu thị "không có đặc tính A". Khi này ta có $p = E(X)$, bài toán ước lượng tỉ lệ được đưa về bài toán ước lượng giá trị kì vọng. Khi đó, ta lập mẫu ngẫu nhiên kích thước $n$. Gọi $\hat{P}$ là thống kê tỉ lệ mẫu ngẫu nhiên, dễ thấy $\hat{P} = \overline{X}$. Giá trị của thống kê này được kí hiệu là $\hat{p}$.

Do $X$ không có phân phối chuẩn, phương sai chưa biết, ta xác định khoảng tin cậy đối xứng của $p$ như sau:
$$\big(\overline{X}-z_{\frac{\alpha}{2}}\frac{S}{\sqrt{n}} ; \overline{X}+z_{\frac{\alpha}{2}}\frac{S}{\sqrt{n}}\big)$$
Ta có $\overline{X} = \hat{P}$ và $S^2 = p(1-p)$, khoảng tin cậy này trở thành
$$\bigg(\hat{P}-z_{\frac{\alpha}{2}}\sqrt{\frac{p(1-p)}{n}} ; \hat{P}+z_{\frac{\alpha}{2}}\sqrt{\frac{p(1-p)}{n}}\bigg)$$
Xấp xỉ $p$ bằng $\hat{P}$, ta có khoảng tin cậy đối xứng của $p$ với độ tin cậy $1-\alpha$
$$\bigg(\hat{P}-z_{\frac{\alpha}{2}}\sqrt{\frac{\hat{P}(1-\hat{P})}{n}} ; \hat{P}+z_{\frac{\alpha}{2}}\sqrt{\frac{\hat{P}(1-\hat{P})}{n}}\bigg)$$
Khoảng tin cậy đối đa của $p$ với độ tin cậy $1-\alpha$
$$\bigg(0; \hat{P}+z_{\alpha}\sqrt{\frac{\hat{P}(1-\hat{P})}{n}}\bigg)$$
Khoảng tin cậy tối thiểu của $p$ với độ tin cậy $1-\alpha$
$$\bigg(\hat{P}-z_{\alpha}\sqrt{\frac{\hat{P}(1-\hat{P})}{n}}; 1\bigg)$$

