---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 3
unit: 3
title: Ước lượng điểm
---
# Ước lượng điểm
## Khái niệm
Xét một [[mi2021_tong_the_va_mau|tổng thể]] với đặc tính cần quan sát được biểu thị bằng biến ngẫu nhiên $X$. Tham số $\theta$ là một đặc trưng (kỳ vọng, phương sai, tỉ lệ,...) của $X$. Do ta không thể khảo sát toàn bộ tổng thể để tìm chính xác $\theta$, ta cần _ước lượng_ $\theta$ theo mẫu. Theo đó, lập [[mi2021_mau_ngau_nhien#Mẫu ngẫu nhiên và thống kê|mẫu ngẫu nhiên]] $\{X_1; X_2;...;X_n\}$ và chọn một thống kê $\hat{\Theta}$ để ước lượng cho $\theta$. Khi $\hat{\Theta}$ nhận giá trị cụ thể, giá trị này được gọi là **giá trị ước lượng** của $\theta$.

Một ước lượng được gọi là **không chệch** nếu
$$E(\hat{\Theta}) = \theta$$
Nếu ước lượng là ước lượng chệch, $|E(\hat{\Theta}) - \theta|$ được gọi là **độ chệch** của ước lượng.
**Sai số bình phương trung bình** của ước lượng được định nghĩa như sau:
$$MSE(\hat{\Theta}) = E((\hat{\Theta} - \theta)^2) = (E(\hat{\Theta})-\theta)^2 + V(\hat{\Theta})$$
Như vậy, để tìm ước lượng có sai số nhỏ nhất, ta thường xét ước lượng có phương sai nhỏ nhất trong các ước lượng không chệch.
## Ước lượng điểm của kỳ vọng, phương sai và tỉ lệ
Do $E(\bar{X}) = \mu$ nên $\bar{X}$ là một ước lượng không chệch của $\mu$. Ta cũng chứng minh được $V(\bar{X})$ là nhỏ nhất trong các ước lượng không chệch của $\mu$.
Do $E(\hat{S}^2) = \frac{n-1}{n}\sigma^2$, $\hat{S}^2$ là một ước lượng chệch của $\sigma^2$. Để có ước lượng không chệch, ta cần _hiệu chỉnh_ $\hat{S}^2$:
$$S^2 = \frac{n}{n-1}\hat{S}^2 = \frac{1}{n-1}\sum_{i = 1}^n{(X_i - \overline{X})^2}$$
Thống kê trên được gọi là **phương sai mẫu ngẫu nhiên đã hiệu chỉnh**. Khi mẫu ngẫu nhiên nhận giá trị cụ thể, ta có giá trị cụ thể $s^2$ là **phương sai mẫu đã hiệu chỉnh**

$$s^2 = \frac{1}{n-1}\sum_{i=1}^n{(x_i - \bar{x})^2} = \frac{1}{n-1}\sum_{i=1}^n{n_i(a_i - \bar{x})^2}$$
