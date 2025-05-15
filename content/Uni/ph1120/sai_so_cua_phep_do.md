---
tags:
  - university
  - note
subject: "[[ph1120]]"
subject-code: ph1120
chapter: 0
unit: 3
title: Sai số của phép đo
---

# Sai số của phép đo
## Định nghĩa, phân loại
- **Sai số** là giá trị đo được không hoàn toàn đúng so với giá trị thực thế
- Phân loại:
	- Sai số hệ thống
	- Sai số ngẫu nhiên
	- Sai số dụng cụ
	- Sai số khách quan
## Sai số của phép đo trực tiếp
- Thực hiện $n$ phép đo thu được $n$ kết quả đo từ $A_1$ đến $A_n$.
- Giá trị trung bình:
$$\overline{A} = \frac{\sum_{i = 1}^n{A_i}}{n}$$
- Sai số tuyệt đối của mỗi lần đo:
$$\Delta A_i = |A_i - \overline{A}|$$
$$\overline{\Delta A} = \frac{\sum_{i = 1}^n{\Delta A_i}}{n}$$
- Sai số dụng cụ:
	- Với dụng cụ đo cơ khí, đồng hồ điện tử: một hoặc nửa ĐCNN
	- Với đồng hồ điện dạng kim: giá trị lớn nhất đo được nhân với cấp chính xác của đồng hồ
- Sai số của phép đo:
$$\Delta A = \overline{\Delta A} + \text{Sai số dụng cụ}$$

## Kết quả đo
- Kết quả: $A = \bar{A} \pm \Delta A$
- Quy tắc chữ số có nghĩa:
	- Sai số của phép đo lấy tối đa 2 chữ số, tính từ **chữ số có nghĩa** (khác không) đầu tiên từ trái sang phải
	- Sai số lấy bao nhiêu chữ số thì kết quả lấy bấy nhiêu chữ số

## Sai số của phép đo gián tiếp
- Cho đại lượng A là hàm số của các đại lượng x,y,z (nhiều hơn tương tự): $A = F(x,y,z)$
- Qua phép đo trực tiếp ta được: $x = \bar{x} \pm \Delta x$; $y = \bar{y} \pm \Delta y$; $z = \bar{z} \pm \Delta z$
- Ta có: 
$$\bar{A} = F(\bar{x}, \bar{y}, \bar{z})$$
- Xác định sai số: Cách 1:
$$\Delta A = F'_x \Delta x + F'_y \Delta y + F'_z \Delta z$$
