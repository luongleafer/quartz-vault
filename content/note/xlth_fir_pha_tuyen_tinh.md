---
tags:
  - note
  - university
subject: "[[it4172]]"
chapter: 3
unit: 2
title: Bộ lọc số FIR pha tuyến tính
---
# Bộ lọc số FIR pha tuyến tính
## Các loại bộ lọc FIR
Xét bộ [[xlth_bo_loc_so|bộ lọc số]] có [[xlth_bieu_dien_he_thong_roi_rac_mien_tan_so|đáp ứng tần số]] là $H(\omega)$, trong đó đáp ứng pha là $\theta(\omega)$. Bộ lọc số FIR pha tuyến tính là bộ lọc có $\tau(\omega) = -\theta'(\omega)$ là hằng số. Khi đó $\theta(\omega)$ có dạng $-\alpha \omega + \beta$
Ta có 4 loại bộ lọc FIR pha tuyến tính:
- Với $\beta = 0$, $\alpha = \frac{N-1}{2}$, $h(n)$ đối xứng, hay $h(n) = h(N-1-n)$
	- Loại 1: $N$ lẻ
	- Loại 2: $N$ chẵn
- Với $\beta \neq 0$, $\alpha = \frac{N-1}{2}$, $\beta = \pm \frac{\pi}{2}$, $h(n) = -h(N-1-n)$, hay $h(n)$ phản đối xứng:
	- Loại 3: $N$ lẻ
	- Loại 4: $N$ chẵn
Đặc điểm của từng loại bộ lọc số:
- Loại 2: $H(\pi) = 0$ nên không thích hợp cho bộ lọc thông cao và chắn dải
- Loại 3: $H(0) = H(\pi) = 0$ nên thích hợp cho bộ lọc thông dải
- Loại 4: $H(0) = 0$ nên thích hợp cho bộ lọc thông dải và thông cao. 

## Tổng hợp bộ lọc FIR pha tuyến tính sử dụng phương pháp cửa sổ
### Thực hiện FIR bằng cửa sổ
Từ bộ lọc lý tưởng (không nhân quả, đáp ứng xung có chiều dài vô hạn), ta sử dụng một **hàm cửa sổ** để tạo ra một bộ lọc FIR nhân quả, pha tuyến tính.
Giả sử ta có bộ lọc lí tưởng với đáp ứng xung $h_d(n)$. Ta cần xây dựng bộ lọc với đáp ứng xung hữu hạn, chiều dài $M$, khi đó ta xây dựng
$$h(n) = \begin{cases}h_d(n) \quad 0 \le n \le M-1\\0 \quad \text{n còn lại}\end{cases}$$
Đặt
$$w_n = \begin{cases}1\quad 0 \le n \le M-1\\ 0 \quad \text{n còn lại}\end{cases}$$
ta có $h(n) = h_d(n)w_n$, trong miền tần số, điều này tương ứng với
$$H(\omega) = H_d(\omega) * W(\omega) = \frac{1}{2\pi}\int_{-\pi}^\pi W(\gamma)H_d(\omega - \gamma)d\gamma$$
Độ rộng búp sóng chính của $W(\omega)$ tỉ lệ với $\frac{1}{M}$. Độ rộng này quyết định độ rộng của dải quá độ. Các búp phụ tạo ra các gợn sóng có dạng giống nhau trong dải thông và dải chắn.

### Các loại cửa sổ

| Tên             | Hàm cửa sổ trong đoạn $[0;M-1]$                                                                                                            | Bề rộng búp sóng chính | Tỉ số biên độ giữa đỉnh thứ cấp đầu tiên và đỉnh trung tâm |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------- | ---------------------------------------------------------- |
| Cửa sổ chữ nhật | $w(n) = 1$                                                                                                                                 | $\frac{4\pi}{M}$       | -13 dB                                                     |
| Cửa sổ tam giác | $w(n) = \begin{cases}\frac{2n}{M-1} \quad (0 \le n \le \frac{M-1}{2})\\ 2 - \frac{2n}{M-1} \quad (\frac{M-1}{2} \le n \le M-1)\end{cases}$ | $\frac{8\pi}{M}$       | -26 dB                                                     |
| Cửa sổ Hanning  | $w(n) = 0,5 \left[ 1 - \cos \left( \frac{2\pi n}{M - 1} \right) \right]$                                                                   | $\frac{8\pi}{M}$       | -32 dB                                                     |
| Cửa sổ Hamming  | $w(n) = 0,54 - 0,46\cos\left(\frac{2\pi n}{M - 1}\right)$                                                                                  | $\frac{8\pi}{M}$       | -43 dB                                                     |
| Cửa sổ Blackman | $w(n) = 0.42 - 0.5\cos\left(\frac{2\pi n}{M-1}\right) + 0.08\cos\left(\frac{4\pi n}{M-1}\right)$                                           | $\frac{12\pi}{M}$      | -57 dB                                                     |
