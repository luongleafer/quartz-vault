---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 1
unit: 1
title: Phép thử và sự kiện
date: 2025-09-22
---
# Phép thử và sự kiện
- **Phép thử ngẫu nhiên:** là một thí nghiệm hay hành động mà:
    - Kết quả không thể đoán trước.
    - Có thể xác định được tập hợp tất cả các kết quả có thể xảy ra.
    - Ví dụ: Xúc xắc.
- **Kết cục sơ cấp** là kết quả không thể chia nhỏ được nữa
- **Không gian mẫu (Ω):** Tập hợp tất cả các kết quả có thể xảy ra của một phép thử.
    - Ví dụ: Gieo xúc xắc 1 lần, $\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5, \omega_6\}$ ($\omega_i$ là kết cục xúc xắc nên mặt có $i$ chấm)
- **"Sự kiện / Biến cố":** là 1 tập con của không gian mẫu $\Omega$.
    - Kí hiệu: A, B, C, ...
    - Ví dụ: A: Sự kiện xuất hiện mặt chẵn.
        - A = {ω₂, ω₄, ω₆} ⊂ Ω (A là tập con của Ω).
- **Sự kiện rỗng (∅):** Không thể xảy ra.
- **Sự kiện chắc chắn (Ω):** Chắc chắn xảy ra.
- **Phép toán trên sự kiện:**
    - **Giao (∩):** A ∩ B = A.B
        - Ý nghĩa: A **và** B **cùng xảy ra**.
    - **Hợp / Tổng (∪):** A ∪ B = A + B
        - Ý nghĩa: **Ít nhất 1 trong** A **hoặc** B **xảy ra**.
    - **Hiệu**: $A \setminus B$
	    - A xảy ra nhưng B không xảy ra
	- **Phần bù/ sự kiện đối**: $\bar{A} = \Omega \setminus A$
- **Tính chất của phép toán**
	- $A \setminus B = A\cap \overline{B} = A\setminus(AB)$
	- $A = AB + A\overline{B}$
	- Luật De Morgan:
		- $\overline{A} + \overline{B} = \overline{AB}$
		- $\overline{A}\overline{B} = \overline{A+B}$
- $A$ và $B$ được gọi là **xung khắc** nếu $AB = \emptyset$
- Giải tích tổ hợp: từ $n$ phần tử, chọn ra $k$ phần tử:
	- Có thứ tự: mỗi cách chọn được gọi là một **chỉnh hợp** chập $k$ của $n$ phần tử:
		- Số chỉnh hợp lặp: $\tilde{A}_n^k = n^k$
		- Số chỉnh hợp không lặp: $A_n^k = \frac{n!}{(n-k)!}$
		- **Hoán vị** là trường hợp đặc biệt của chỉnh hợp lặp, khi $k = n$, số hoán vị $P_n = n!$
	- Không có thứ tự: mỗi cách chọn được gọi là một **tổ hợp** chập $k$ của $n$ phần tử. Số tổ hợp không lặp: $C_n^k = \frac{n!}{(n-k)!.k!}$
