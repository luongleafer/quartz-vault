---
aliases:
share: false
tags:
  - university
  - note
subject: "[[it3420]]"
chapter: 2
unit: 3
title: Phân tích một chiều diode
---
# Phân tích một chiều [[dt_diode_definition|diode]]
## Diode lý tưởng
- Khi phân cực ngược, tương đương hở mạch
- Khi phân cực thuận, tương đương ngắn mạch
## Mô hình tuyến tính từng đoạn
- Xấp xỉ [[dt_diode_states#Trạng thái phân cực thuận|đặc tính Volt-Ampere]] tuyến tính theo từng đoạn thẳng.
- Nhận xét: tồn tại giá trị $V_{\gamma}$
	- Khi $V_D > V_\gamma$, đường đặc tính V-A xấp xỉ một đường thẳng với độ nghiêng $\frac{1}{r_f}$
		- Gọi $r_f$ là _điện trở phân cực thuận_
		- $V_\gamma$ là _điện áp ngưỡng_
	- Khi $V_D < V_\gamma$, đường đặc tính V-A xấp xỉ một đường thẳng song song với trục hoành và rất sát trục hoành, có thể coi $V_D= 0$ và $I_D = 0$
- $r_f$ tương đối nhỏ, trong mạch một chiều với tải lớn có thể coi $r_f = 0$, khi đó $V_D$ là hằng số và bằng $V_\gamma$ ở trạng thái phân cực thuận.

