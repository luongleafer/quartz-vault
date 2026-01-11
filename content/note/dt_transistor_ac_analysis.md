---
tags:
  - note
  - university
subject: "[[it3420]]"
chapter: 3
unit: 4
title: Phân tích xoay chiều transistor
---
# Phân tích xoay chiều transistor

## Đặc tính truyền điện áp
- Sau khi thực hiện [[dt_transistor_dc_analysis|phân tích một chiều transistor]], ta thu được đường **đặc tính truyền điện áp** sau:
![[Pasted image 20251104072545.png]]
- Trong đó $V_I$ là $V_{BB}$ và $V_O$ là $V_{CE}$
- Nếu đầu vào $V_{BB}$ là một điện áp xoay chiều $v_I$, ta có thể thu được một điện áp xoay chiều có dạng sóng tương tự (nhưng được khuếch đại và ngược chiều) ở đầu ra
![[Pasted image 20251104072907.png]]
- Nếu $v_I$ không đủ nhỏ, điện áp có thể dao động quá lớn xung quanh điểm làm việc $Q$, chạm tới các vùng khác như vùng bão hòa hoặc vùng khóa.
- Để việc khuếch đại ổn định trong vùng tích cực thuận, $v_I$ cần có biên độ đủ nhỏ. Khi này $v_I$ được gọi là **tín hiệu nhỏ**

## Phân tích xoay chiều
Để phân tích xoay chiều ta thực hiện theo các bước:
- Coi tín hiệu xoay chiều là ngắn mạch và Phân tích một chiều, tìm điểm làm việc $Q$
- Thay transistor bằng mô hình tương đương tín hiệu nhỏ (mạch $\pi$ lai)
- Phân tích mạch tín hiệu nhỏ tương đương
- Xếp chồng kết quả: lấy tổng của giá trị một chiều và giá trị xoay chiều tức thời
## Mô hình tương đương tín hiệu nhỏ
- Thực hiện thay thế:
	- Đầu vào $B-E$ tương đương **điện trở tín hiệu nhỏ** $r_\pi$
	- Đầu $C-E$ tương đương một **nguồn dòng** với hệ số dẫn truyền $g_m$
![[Pasted image 20251104073514.png]]
- Ta có:
$$r_\pi = \frac{V_T}{I_{BQ}}$$
$$g_m = \frac{I_{CQ}}{V_T}$$
với $V_T = 0,026 (V)$

## Phân tích mạch tín hiệu nhỏ
- Điện áp đầu ra
$$V_O = V_{CE} = -(g_m V_\pi)R_C$$
- Điện áp hạ trên $r_\pi$:
$$V_\pi = V_S\frac{r_\pi}{r_\pi + R_B}$$
- Hệ số khuếch đại điện áp:
$$A_v = \frac{V_O}{V_S} = -(g_mR_C)\frac{r_\pi}{r_\pi + R_B}$$
## Hiệu ứng Early
- Là hiện tượng độ rộng vùng Base bị thu hẹp khi $V_{CB}$ tăng, làm cho $I_C$ tăng nhẹ khi $V_{BE}$ không đổi.
- Hiệu ứng này làm giảm hệ số khuếch đại điện áp nhỏ trong mạch E chung
- Khi xét đến hiệu ứng Early, trong mạch tương đương xoay chiều xuất hiện $r_o$ giữa $C-E$
$$r_o = \frac{V_A}{I_{CQ}}$$
- $V_A$ được gọi là **điện thế Early**
- Khi đó
$$A_v = -gm(RC || r_o)\frac{r_\pi}{r_\pi+R_B}$$
