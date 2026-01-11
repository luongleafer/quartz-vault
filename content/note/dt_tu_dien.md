---
tags:
  - note
  - university
subject: "[[it3420]]"
chapter: 1
unit: 2
title: Tụ điện
---
# Tụ điện
- Là _linh kiện điện tử thụ động_ tạo bởi hai bề mặt dẫn điện, ngăn cách bởi điện môi.
- Xem thêm: [[tu_dien|Tụ điện, PH1120]]
- Quá trình nạp: 
	- Khi cấp nguồn điện một chiều cho tụ điện, tụ bắt đầu quá trình nạp
	- Giả sử tụ được nối với nguồn $E$ nối tiếp với điện trở $R$
	- Dòng điện qua tụ sẽ giảm dần theo công thức $$i_C = \frac{E}{R}e^\frac{-t}{\tau}$$ với $\tau = RC$
	- Sau quá trình nạp, đối với điện một chiều, tụ điện coi như _hở mạch_
	- Quá trình nạp thường kết thúc sau thời gian $5\tau$, tại thời điểm này, $i_C$ chỉ còn khoảng $1\%$ so với $\frac{E}{R}$
	- Điện áp giữa hai bản tụ điện được tính theo công thức $$v_C = E - i_C \times R = E(1- e^\frac{-t}{\tau})$$
- Quá trình xả:
	- Được thực hiện thông qua một điện trở
	- Giả sử trước bước xả, tụ điện có điện áp $V_i$
	- Điện áp giữa hai bản tụ điện giảm dần theo công thức $$v_c = V_i e^\frac{-t}{\tau}$$
	- Dòng điện cũng giảm dần theo công thức $$i_c = \frac{v_c}{R} $$
- Công dụng của tụ điện:
	- Lưu trữ điện năng
	- Cho phép điện áp xoay chiều đi qua
	- Cản dòng điện một chiều
	- Lọc điện áp xoay chiều thành điện áp một chiều
