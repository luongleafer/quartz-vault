---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 4
unit: 2
title: Kiểm định giá trị kì vọng
---
# Kiểm định giá trị kỳ vọng
Ta xét [[xstk_bai_toan_kiem_dinh|bài toán kiểm định]] mà tham số cần kiểm định là kỳ vọng $\mu$ của tổng thể.
## Kiểm định một giá trị kỳ vọng
Xét $X$ là một đại lượng trong tổng thể, có kỳ vọng $\mu$. Xây dựng mẫu ngẫu nhiên kích thước $n$ có trung bình mẫu ngẫu nhiên là $\bar{X}$, phương sai mẫu ngẫu nhiên đã hiệu chỉnh là $S$. Lấy mẫu cụ thể, ta đưa ra đối thuyết về giá trị $\mu$. Lập giả thuyết không $H_0: \mu = \mu_0$.

### Trường hợp $X$ có phương sai đã biết $\sigma^2$

Xét thống kê
$$Z = \frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{n}}}$$
Thống kê $Z$ có phân phối chuẩn tắc nếu $X$ có phân phối chuẩn, và xấp xỉ phân phối chuẩn tắc nếu $X$ không có phân phối chuẩn, nhưng kích thước mẫu đủ lớn.

Khi $H_0$ đúng, ta có tiêu chuẩn kiểm định
$$Z_0 = \frac{\bar{X}-\mu_0}{\frac{\sigma}{\sqrt{n}}}$$
Dựa trên đối thuyết, ta có miền bác bỏ:
- Nếu đối thuyết có dạng $\mu > \mu_0$, miền bác bỏ là $(z_\alpha; +\infty)$
- Nếu đối thuyết có dạng $\mu < \mu_0$, miền bác bỏ là $(-\infty; -z_\alpha)$
- Nếu đối thuyết có dạng $\mu \neq \mu_0$, miền bác bỏ là $(-\infty; -z_\frac{\alpha}{2}) \cup (z_\frac{\alpha}{2};+\infty)$
Xét biến quan sát dựa trên mẫu
$$z_{qs} = \frac{\bar{x}-\mu_0}{\frac{\sigma}{\sqrt{n}}}$$
Nếu $z_{qs} \in W_\alpha$, ta bác bỏ $H_0$.
### Trường hợp $X$ có phân phối chuẩn với phương sai chưa biết
Ta có thống kê
$$T = \frac{\bar{X}-\mu}{\frac{S}{\sqrt{n}}}$$ có phân phối Student với $n-1$ bậc tự do.

Khi $H_0$ đúng, ta có tiêu chuẩn kiểm định
$$T_0 = \frac{\bar{X}-\mu_0}{\frac{S}{\sqrt{n}}}$$
Dựa trên đối thuyết, ta có các miền bác bỏ:
- Nếu đối thuyết có dạng $\mu > \mu_0$, miền bác bỏ là $(t_{n-1;\alpha}; +\infty)$
- Nếu đối thuyết có dạng $\mu < \mu_0$, miền bác bỏ là $(-\infty; -t_{n-1;\alpha})$
- Nếu đối thuyết có dạng $\mu \neq \mu_0$, miền bác bỏ là $(-\infty; -t_{n-1;\frac{\alpha}{2}}) \cup (t_{n-1;\frac{\alpha}{2}};+\infty)$

Xét biến quan sát
$$t_{qs} = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}}$$
Nếu $t_{qs} \in W_\alpha$, ta bác bỏ $H_0$

### Trường hợp $X$ không có phân phối chuẩn, phương sai chưa biết, kích thước mẫu đủ lớn
Ta có thống kê
$$T = \frac{\bar{X}-\mu}{\frac{S}{\sqrt{n}}}$$có phân phối xác suất xấp xỉ phân phối chuẩn tắc
Khi $H_0$ đúng, ta có tiêu chuẩn kiểm định
$$T_0 = \frac{\bar{X}-\mu_0}{\frac{S}{\sqrt{n}}}$$
Dựa trên đối thuyết, ta có miền bác bỏ:
- Nếu đối thuyết có dạng $\mu > \mu_0$, miền bác bỏ là $(z_\alpha; +\infty)$
- Nếu đối thuyết có dạng $\mu < \mu_0$, miền bác bỏ là $(-\infty; -z_\alpha)$
- Nếu đối thuyết có dạng $\mu \neq \mu_0$, miền bác bỏ là $(-\infty; -z_\frac{\alpha}{2}) \cup (z_\frac{\alpha}{2};+\infty)$

Xét biến quan sát
$$t_{qs} = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}}$$
Nếu $t_{qs} \in W_\alpha$, ta bác bỏ $H_0$