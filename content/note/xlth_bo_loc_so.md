---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 3
unit: 1
title: Bộ lọc số
---
# Bộ lọc số
**Bộ lọc số** là bộ lọc cho phép loại bỏ các tín hiệu trong một tần số nào đó.
Bộ lọc số hoạt động theo cách điều chỉnh [[xlth_bieu_dien_he_thong_roi_rac_mien_tan_so|đáp ứng biên độ]] của các thành phần tần số.
## Bộ lọc thông thấp lý tưởng
Bộ lọc thông thấp là bộ lọc chỉ cho các tín hiệu thấp hơn một tần số cắt $\omega_C$ đi qua. Đáp ứng biên độ của bộ lọc thông thấp lý tưởng là 
$$|H(\omega)| = \begin{cases}1 \quad |\omega| \le \omega_C \\ 0 \quad \omega_C < |\omega| \le \pi  \end{cases}$$
Khi đó, $\omega_C$ được gọi là **tần số cắt**, đoạn $[-\omega_C; \omega_C]$ được gọi là **dải thông** và phần còn lại trong đoạn $[-\pi, \pi]$ được gọi là **dải chắn**
Khi đó đáp ứng xung của bộ lọc là 
$$h_{lp}(n) = \begin{cases} \frac{\sin(\omega_C n)}{\pi n} \quad n \neq 0\\ \frac{\omega_C}{\pi} \quad n = 0 \end{cases}$$
## Bộ lọc thông cao lý tưởng
Bộ lọc thông cao ngược lại với bộ lọc thông thấp, chỉ cho tần số lớn hơn $\omega_C$ đi qua.
$$|H(\omega)| = \begin{cases}0 \quad |\omega| < \omega_C \\ 1 \quad \omega_C \le |\omega| \le \pi  \end{cases}$$
Khi đó đáp ứng xung
$$h_{lp}(n) = \begin{cases} -\frac{\sin(\omega_C n)}{\pi n} \quad n \neq 0\\ 1-\frac{\omega_C}{\pi} \quad n = 0 \end{cases}$$
## Bộ lọc thông dải lí tưởng
$$|H(\omega)| = \begin{cases}1 \quad \omega_{C1} \le |\omega| \le \omega_{C2} \\ 0 \quad \omega \text{ còn lại }  \end{cases}$$

$$h(n) = \begin{cases} \frac{\sin(\omega_{C2} n) - \sin(\omega_{C1}n)}{\pi n} \quad n \neq 0\\ \frac{\omega_{C2}-\omega_{C1}}{\pi} \quad n = 0 \end{cases}$$

## Bộ lọc chắn dải lí tưởng
$$|H(\omega)| = \begin{cases}1 \quad |\omega| \le \omega_{C1} \text{ hoặc }\omega_{C2} \le |\omega| \le \pi \\ 0 \quad \omega \text{ còn lại }  \end{cases}$$
$$h(n) = \begin{cases} \frac{\sin(\omega_{C1} n) - \sin(\omega_{C2}n)}{\pi n} \quad n \neq 0\\ 1+ \frac{\omega_{C1}-\omega_{C2}}{\pi} \quad n = 0 \end{cases}$$
