---
tags:
  - note
  - university
subject: "[[it3420]]"
chapter: 1
unit: 3
title: Cuộn cảm
---
# Cuộn cảm
- Là linh kiện điện tử thụ động, dùng để chứa từ trường
- Được tạo ra từ dây dẫn điện quấn thành nhiều vòng.
- Sinh ra từ trường cảm ứng hãm lại sự biến thiên dòng điện trong cuộn dây

- Quá trình nạp
	- Nối cuộn cảm với điện trở và nguồn
	- Khi đóng công tắc, dòng điện tức thời = 0, cuộn cảm coi như hở mạch
	- Dòng điện qua cuộn tăng dần cho đến khi điện áp rơi trên tụ = 0, cuộn coi như ngắn mạch
	- Công thức dòng điện qua cuộn: $$i_L = \frac{E}{R}(1 - e^\frac{-t}{\tau})$$ với $\tau = \frac{L}{R}$
	- Điện áp rơi trên cuộn cảm $$v_L = Ee^\frac{-t}{\tau}$$
	- Quá trình nạp được coi như kết thúc sau $5\tau$
- Quá trình xả
	- Khi mở khóa, ta cần nối thêm một điện trở $R_2$ thay cho nguồn
	- Giả sử sau khi nạp, dòng điện trên cuộn là $I_i$, khi xả, dòng điện sẽ giảm dần: $$i_L = I_i e^\frac{-t}{\tau '}$$ với  $\tau' = \frac{L}{R_1 + R_2}$
	- Điện áp rơi trên cuộn $$v_L = -V_ie^\frac{-t}{\tau '}$$ với $V_i = I_i(R_1 + R_2)$
- Công dụng:
	- Dẫn dòng một chiều, ngăn dòng xoay chiều
	- Tạo mạch cộng hưởng
