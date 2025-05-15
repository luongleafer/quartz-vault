---
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 4
unit: 13
title: Những đặc trưng của dòng điện
---
# Những đặc trưng của dòng điện
## Cường độ dòng điện
- Dòng điện là dòng _chuyển dời có hướng_ của điện tích
- Chiều của dòng điện là chiều chuyển dời của _điện tích dương_
- **Cường độ dòng điện** là đại lượng đặc trưng cho mức độ mạnh yếu của dòng điện qua một đơn vị diện tích cho trước
$$i = \frac{dq}{dt}$$
## Vector mật độ dòng điện
- là đại lượng đặc trưng cho độ mạnh yếu tại mỗi điểm, phương và chiều dòng điện
$$J = \frac{dI}{dS_n}$$
- Vector mật độ dòng điện có:
	- Điểm đặt: điểm trên tiết diện vuông góc với chiều dòng điện
	- Phương: cùng phương với dòng điện
	- Chiều: cùng chiều chuyển động của điện tích dương
- Từ đó ta có

$$dI = JdSn = \overrightarrow{J}.\overrightarrow{dS} \Rightarrow  I = \int{\overrightarrow{J}.\overrightarrow{dS}}$$
- Nếu dòng điện là dòng chuyển dời có hướng của điện tích dương có cùng vận tốc $v$ và mật độ điện tích $n_0$, ta có
$$\overrightarrow{J} = n_0q\overrightarrow{v}$$
## Định luật Ohm dạng vi phân
- Xét khối [[vat_dan|vật dẫn]] có [[dien_the|điện thế]] hai đầu là $V$ và $V+dV (dV < 0)$, chiều dài $dl$, diện tích $dS$
- Với dòng điện một chiều, không đổi, ta có
$$I = \frac{U}{R} = \frac{V_1-V_2}{R}$$
- Với dòng điện biến đổi, chia vật thành các vi phân mà trong mỗi khối vi phân đó, [[dien_truong|điện trường]] là điện trường đều, ta có
$$dI = \frac{-dV}{R}$$
Ta có:
$$R = \frac{\rho dl}{dS}$$
vậy
$$dI = \frac{1}{\rho}\bigg(\frac{-dV}{dl}\bigg)dS \Rightarrow \frac{dI}{dS} = \frac{1}{\rho}\overrightarrow{E}dS$$
Đặt $\sigma = \frac{1}{\rho}$, đại lượng này được gọi là **điện dẫn xuất**, ta có
$$\frac{dI}{dS} = \sigma \overrightarrow{E}$$
>[!formula] Định luật Ohm dạng vi phân
>$$\overrightarrow{J} = \sigma \overrightarrow{E}$$

## Nguồn điện
- Để duy trì dòng điện, ta phải đưa điện tích dương từ nơi có điện thế thấp đến nơi có điện thế cao. Lực tác dụng để thực hiện việc này là lực phi tĩnh điện, được gọi là **lực lạ**
- **Trường lạ** là trường gây ra lực lạ
- **Nguồn điện** là nguồn tạo ra trường lạ
- **Suất điện động** là công của lực tĩnh điện dịch chuyển điện tích đi 1 vòng trong mạch kín của nguồn
$$\epsilon = \frac{A}{q}$$
- Xét nguồn điện có trường lạ $\overrightarrow{E^\star}$
- Theo định nghĩa

$$\epsilon = \frac{A}{q} = \frac{\oint{q(\vec{E} + \vec{E^\star})\vec{ds}}}{q} = \oint{(\overrightarrow{E} + \overrightarrow{E^\star})\overrightarrow{ds}}$$
- Do tính thế của trường tĩnh điện, ta có $$\oint{\overrightarrow{E}\,\overrightarrow{ds}}  = 0$$
>[!formula] Suất điện động
>$$\epsilon = \oint{\overrightarrow{E} \cdot \overrightarrow{ds}}$$
