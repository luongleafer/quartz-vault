---
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 4
unit: 16
title: Từ thông
---
# Từ thông
## Từ thông
>[!definition] Đường sức từ
>- Là những đường cong mà tiếp tuyến của chúng tại mỗi điểm là [[tu_truong#Vector cảm ứng từ|vector cảm ứng từ]] tại điểm đó
>- Chiều của đường sức từ là chiều của $\vec{B}$
>- Tập hợp các đường sức được gọi là **từ phổ**

- Tính chất của đường sức từ:
	- Đường cong, kín
	- Không bao giờ cắt nhau
	- Thể hiện hình ảnh và tính chất của từ trường
		- Đường sức thưa: từ trường yếu
		- Đường sức mau: từ trường mạnh
		- Đường sức song song, cách đều: từ trường đều

>[!definition] Từ thông
>là số đường sức từ gửi qua một mặt $S$

- Để xác định từ thông, ta chia $S$ thành những mảnh $dS$ vô cùng nhỏ mà trên các mảnh này, từ trường là từ trường đều, khi đó, vi phân từ thông
$$d\phi = \vec{B}\cdot\vec{dS} = B\cos\alpha dS$$ với $\alpha$ là góc tạo bởi $\vec{B}$ và vector pháp tuyến của $dS$
## Định luật Gauss đối với từ trường
- Xét từ thông gửi qua mặt $S$ là mặt kín. Các đường sức từ đi vào $S$ sẽ có $\alpha$ là góc tù, và các đường sức đi ra khỏi $S$ sẽ có $\alpha$ là góc nhọn.
- Từ thông tổng hợp $\phi = \phi_v - \phi_r$. Do số đường vào bằng với số đường ra nên $\phi = 0$ 
>[!formula] Định luật Gauss đối với từ trường
>Từ thông gửi qua một mặt kín bằng 0
>$$\oint_{S}{\vec{B}\vec{dS}} = 0$$

- Định luật Gauss thể hiện _tính xoáy_ của từ trường
## Định lí Ampere về dòng điện toàn phần
**Lưu số** của vector cường độ từ trường trên đường cong kín $(C)$ là
$$\oint_{(C)}{\vec{H}\vec{dl}}$$
Xét dòng điện thẳng dài vô hạn và đường cong $(C)$ bao quanh dòng điện
![[luu_so_cuong_do_tu_truong_nam_trong.excalidraw]]
Ta có
$$\vec{H}\vec{dl} = Hdl\cos\alpha = Hrd\varphi$$
Lưu số của vector cường độ từ trường trên $C$. Xét chiều lấy tích phân cùng chiều với các đường cảm ứng từ do dòng điện gây ra
$$\oint_{(C)}{\vec{H}\vec{dl}} = \oint_{(C)}{Hrd\varphi} = \frac{I}{2\pi}\oint_{(C)}{d\varphi}$$
Nếu $(C)$ bao xung quanh dòng điện, $\oint_{(C)}{d\varphi} = 2\pi$, tức là 
$$\oint_{(C)}{\vec{H}\vec{dl}} = I$$
Nếu chiều lấy tích phân ngược chiều với chiều cảm ứng từ, ta có
$$\oint_{(C)}{\vec{H}\vec{dl}} = -I$$
Nếu $(C)$ không bao xung quanh dòng điện
$$\oint_{(C)}{d\varphi} = \Delta \varphi - \Delta \varphi = 0$$
Vậy ta có
>[!formula] Định luật Ampere về dòng điện toàn phần
>Lưu số của cường độ từ trường dọc theo đường cong kín $(C)$, bằng tổng đại số các dòng điện đặt trong $(C)$
>$$\oint_{(C)}{\vec{H}\vec{dl}} = \sum{I}$$

- Trong đó, chiều dương của $I$ tuân theo quy tắc bàn tay phải, các ngón tay khom theo chiều lấy tích phân, chiều ngón cái là chiều dương

## Ứng dụng định luật Ampere để tìm cường độ từ trường của các dòng điện đặc biệt
- Xét ống dây hình xuyến, bán kính trung bình là $R$, gồm $n$ vòng dây sít nhau có dòng điện $\vec{I}$ chạy qua. Cường độ từ trường
	- Trong ống xuyến $H = 0$
	- Trong lòng xuyến $H = \frac{nI}{2\pi R}$
	- Bên ngoài xuyến $H = 0$
- Xét ống dây thẳng, thiết diện $S$, chiều dài $l$ gồm $n$ vòng dây sít nhau. Cường độ từ trường bên trong lòng ống dây
$$H = \frac{nI}{l}$$

