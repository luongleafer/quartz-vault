---
aliases:
share: false
tags:
  - university
  - note
subject: "[[it3420]]"
chapter: 3
unit: 2
title: Transistor ở chế độ tích cực thuận
---
# Transistor ở chế độ tích cực thuận
- [[dt_transistor_definition|Transistor]] ở chế độ tích cực thuận khi $V_{BE} >0$ và $V_{BC} <0$
![[Pasted image 20251019091112.png]]
- Xét transistor npn ở chế độ tích cực thuận:
	- Do B-E [[dt_diode_states#Trạng thái phân cực thuận| phân cực thuận]] nên xuất hiện dòng electron từ n sang p, khiến mật độ hạt dẫn thiểu số ở p tăng mạnh
	- Do B-C [[dt_diode_states#Trạng thái phân cực ngược|phân cực ngược]], mật độ electron ở vùng tiếp giáp thấp
	- Dòng electron phóng từ E, khuếch tán qua B, quét qua vùng tiếp giáp B-C và được thu lại ở C
	- 3 dòng điện xuất hiện ở mỗi cực
- Dòng điện ở cực E:
$$i_E= I_{EO}(e^{\frac{v_{BE}}{V_T}} - 1)$$
Do $v_{BE} >> V_T$ nên ta có thể lược bỏ $-1$, từ đó
$$i_E \approx I_{EO}e^{\frac{v_{BE}}{V_T}}$$
Với $I_{EO}$ nằm trong khoảng $10^{-16}$ đến $10^{-12} (A)$, phụ thuộc vào lớp tiếp giáp
- Dòng điện ở cực C:
$$i_C = I_Se^{\frac{v_{BE}}{V_T}}$$
- Dòng điện ở cực $B$, tương tự, cũng phụ thuộc vào $v_{BE}$
- Ở chế độ tích cực thuận, ta luôn có
$$i_C = \beta i_B$$
Hệ số $\beta$ được gọi là **hệ số khuếch đại** của transistor
- Nếu coi cả transistor là một nút đơn, theo định luật Kirchhoff về nút mạch, ta có
$$\begin{aligned}
i_E &= i_C + i_B\\
i_E &= (1+\beta)i_B\\
\Rightarrow i_C &= \frac{\beta}{1+\beta}i_E \\
&= \alpha i_E
\end{aligned}$$
