---
aliases:
share: false
tags:
  - university
  - note
subject: "[[it3420]]"
chapter: 3
unit: 3
title: Phân tích một chiều transistor
---
# Phân tích một chiều transistor
## Bổ sung khái niệm
- **Nguồn áp** là linh kiện hai cực có thể cung cấp _điện áp_ cố định
- **Nguồn dòng** là linh kiện hai cực có thể cung cấp _dòng điện_ không đổi
- [[dt_transistor_definition|Transistor]] mạch E chung là mạch có chung thành phần tín hiệu xoay chiều:
	- Tín hiệu vào từ B-E
	- Tín hiệu được lấy ra ở C-E
	- Tín hiệu vào và ra:
		- Chung thành phần tín hiệu xoay chiều
		- Ngược pha
		- Khuếch đại về biên độ

## Phân tích một chiều mạch E chung
- Xét mạch npn:
![[Pasted image 20251019094153.png]]
- Giả thiết B-E phân cực thuận, khi này $V_{BE} = V_{BE}(on)$
- Ở vòng mạch (1):
$$\begin{aligned}
I_B &= \frac{V_{BB}-V_{BE(on)}}{R_B} \\
I_C &= \beta I_B
\end{aligned}$$
- Ở vòng mạch (2):
$$V_{CE} = V_{CC}-I_CR_C$$
- Nếu $V_{CE} > V_{BE(on)}$, transistor ở [[dt_transistor_active_state|chế độ tích cực thuận]], khi đó:
	- B-E tương đương một [[dt_diode_states#Trạng thái phân cực thuận|diode phân cực thuận]]
	- C-E tương đương nguồn dòng giá trị $\beta I_B$
- Mạch một chiều tương đương:
![[Pasted image 20251019094555.png]]
- Công suất tiêu thụ của transistor:
$$P_T=I_BV_{BE(on)}+I_CV_{CE}\approx I_CV_{CE}$$

## Chế độ bão hòa
- Khi $V_{BB}$ tăng, $I_B$ tăng, kéo theo $I_C$ tăng do hệ số khuếch đại $\beta$.
- Đến một ngưỡng nào đó, khi $I_B$ tăng nhưng $I_C$ _không tăng được nữa_. Ta gọi trạng thái này là **chế độ bão hòa**.
- Ở chế độ bão hòa, $I_C < \beta I_B$.
- $V_{CE(sat)}$ thường ở khoảng $0.1 - 0.3(V)$, tùy linh kiện.
- Nếu ta giả sử mạch hoạt động ở chế độ tích cực thuận, nhưng tính toán được $V_{CE} < 0$, transistor có thể ở trạng thái bão hòa.

## Chế độ khóa
- Khi $V_{BB} < V_{BE(on)}$, diode ở chế độ khóa, lúc này $I_B = I_C = 0$
- Khi đó $V_{CE} = V_{CC}$.
- Nếu ta giả sử mạch hoạt động ở chế độ tíchcực thuận, nhưng tính toán được $I_B < 0$, transistor có thể ở trạng thái khóa

## Phân cực cho transistor
- Mục đích: thiết lập điểm làm việc ổn định cho transistor
- Phân cực bằng một điện trở cực B:
![[Pasted image 20251104071918.png]]
- Phân cực bằng bộ chia điện thế:
![[Pasted image 20251104072009.png]]
- Áp dụng định lí Thevenin, mạch trên tương đương với
![[Pasted image 20251104072038.png]]
Trong đó:
$$V_{TH} = V_{CC}\frac{R_2}{R_1 + R_2}$$
$$R_{TH} = \frac{R_1R_2}{R_1+R_2}$$
- Để thiết kế điểm làm việc $Q$ ổn định, ta chọn $R_{TH} << (1+\beta)R_E$. Khi đó $I_B$ ít phụ thuộc $R_{TH}$ và ít phụ thuộc vào $\beta$
- Khi đó, 
$$I_E \approx \frac{V_{TH} - V_{BE(on)}}{R_E}$$, dòng $I_E$ và $I_C$ gần như độc lập với $\beta$
