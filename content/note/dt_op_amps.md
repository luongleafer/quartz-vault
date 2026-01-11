---
tags:
  - note
  - university
subject: "[[it3420]]"
chapter: 4
unit: 1
title: Khuếch đại thuật toán
---
# Khuếch đại thuật toán
## Khái niệm
- **Khuếch đại thuật toán** (Operational Amplifier), gọi tắt là **op-amp** là một loại mạch khuếch đại điện áp vi sai, được chế tạo dưới dạng mạch tích hợp (IC), có chức năng khuếch đại **chênh lệch điện áp** giữa hai đầu vào, tạo ra một đầu ra duy nhất
- Cấu tạo:
![[Pasted image 20251104074945.png]]
- Gồm:
	- Đầu vào đảo (Inverting input) (1)
	- Đầu vào không đảo (Non-inverting input) (2)
	- Đầu ra (Output) (3)
	- Các chân cấp nguồn phân cực $V^+$ và $V^-$ (thường sẽ được giản lược khi ký hiệu trong mạch)
- Tính chất
	- Trở kháng đầu vào _rất lớn_, có thể coi dòng điện vào xấp xỉ 0
	- Trở kháng ra _rất nhỏ_, có thể coi tương đương $R_o = 0$
	- Hệ số khuếch đại _rất lớn_, trong điều kiện lí tưởng, $A_{od}$ tiệm cận vô cùng
- Thực tế, $V_O$ được giới hạn bởi $V^+$ và $V^-$
$$V^- + \Delta V < V_O < V^+ - \Delta V$$
## Một số mạch cơ bản
### Mạch khuếch đại đảo
![[Pasted image 20251104075337.png]]
- Điện áp vào được nối với đầu vào đảo
- Đầu ra được nối vào đầu vào đảo qua **đường hồi tiếp âm**
- Nếu đầu vào không đảo được nối với đất, hay $v_2 = 0$, ta có $v_1 = 0$, khi này $v_1$ được gọi là _nối đất ảo_ 
![[Pasted image 20251104075714.png]]
- Ta có
$$i_1 = \frac{v_I - v_1}{R_1} = \frac{v_I}{R_1}$$
$$v_O = v_1 - i_2R_2 = - i_1R_2 = v_I \frac{-R_2}{R_1}$$
- Hệ số khuếch đại điện áp
$$A_v = \frac{-R_2}{R_1}$$
## Mạch khuếch đại không đảo
![[Pasted image 20251104075952.png]]
- Điện áp đầu vào được nối với đầu vào không đảo
- Có đường hồi tiếp âm
- Nếu đầu vào đảo nối đất, $v_1$ và $v_2$ luôn bằng nhau, được gọi là _ngắn mạch ảo_
- Ta có
$$\begin{aligned}
i_1 &= \frac{-v_1}{R_1} = \frac{-v_i}{R_1}\\
i_2 &= \frac{v_1 - v_O}{R_2} = \frac{v_I - v_O}{R_2}
\end{aligned}
$$
- Do $i_1 = i_2$ nên
$$\begin{aligned}
&\frac{-v_I}{R_1} = \frac{v_I - v_O}{R_2}\\
\Rightarrow & v_O = v_i\bigg(1+ \frac{R_2}{R_1} \bigg)
\end{aligned}
$$
- Hệ số khuếch đại điện áp
$$A_v = 1+ \frac{R_2}{R_1}$$
- Nếu $R_1 = \infty$ và $R_2 = 0$, ta có **mạch lặp**:
![[Pasted image 20251104080546.png]]
- Mạch lặp có hệ số khuếch đại $A_v = 1$, được sử dụng như một bộ khuếch đại đệm giữa nguồn có trở kháng cao và tải trở kháng thấp

## Bộ so sánh
- Là mạch phát hiện điện áp vượt quá một ngưỡng nào đó
- Không sử dụng đường hồi tiếp âm, đầu ra sẽ bão hòa ở một trong hai trạng thái âm hoặc dương.
- Để phát hiện điện áp mức 0, ta sử dụng mạch sau:
![[Pasted image 20251104080805.png]]
- Đầu vào đảo nối đất, tín hiệu vào đưa vào đầu vào không đảo.
- Khi $v_{in}$ qua điểm 0, $v_{out}$ sẽ "nhảy" giữa hai trạng thái bão hòa
![[Pasted image 20251104080925.png]]
- Để so sánh phát hiện mức khác không, ta mắc đầu vào đảo với điện áp cần so sánh, còn gọi là **điện áp tham chiếu** $V_{REF}$
![[Pasted image 20251104081057.png]]
- Khi này, nếu $v_{in} > V_{REF}$, $v_{out}$ sẽ ở mức bão hòa dương, và ở mức bão hòa âm nếu ngược lại
![[Pasted image 20251104081157.png]]
## Mạch khuếch đại vi sai
- Khuếch đại sự khác nhau giữa hai tín hiệu đầu vào
![[Pasted image 20251104081351.png]]
- Tại nút a:
$$
\begin{aligned}
&\frac{v_1 - v_a}{R_1} = \frac{v_a - v_o}{R_2}\\
\Rightarrow & v_o = \bigg(\frac{R_2}{R_1} + 1\bigg)v_a - \frac{R_2}{R_1}v_1 
\end{aligned}
$$
- Tại nút b:
$$
\begin{aligned}
& \frac{v_2 - v_b}{R_3} = \frac{v_b}{R_4} \\
\Rightarrow & v_b = \frac{R_4}{R_3+R_4} v_2
\end{aligned}
$$
- Do $v_a = v_b$ nên
$$v_o = \frac{R_2+R_1}{R_1}\times \frac{R_4}{R_3+R_4}v_2 - \frac{R_2}{R_1}v_1$$
- Nếu $\frac{R_1}{R_2} = \frac{R_3}{R_4}$ thì
$$v_o = \frac{R_2}{R_1}(v_2 - v_1)$$
## Ứng dụng
- Bộ chuyển đối tín hiệu từ tương tự sang số và ngược lại.