---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 3
unit: 1
title: Tổng thể và mẫu
---
# Tổng thể và mẫu

## Khái niệm tổng thể và mẫu
Trong thực tế, khi nghiên cứu các vấn đề tự nhiên, xã hội, kinh tế,... ta thường dẫn đến _khảo sát_ một hay nhiều _dấu hiệu_ trên _nhiều phần tử_. Tập hợp tất cả các phần tử cần nghiên cứu được gọi là một **tổng thể (đám đông)**. 
Một số tính chất của tổng thể:
- Số phần tử của tổng thể, kí hiệu $N$, có thể là hữu hạn (thường rất lớn) hoặc vô hạn.
- Ta chỉ nghiên cứu một hoặc một vài dấu hiệu nhất định của các phần tử trong tổng thể.
- Ta _không thể_ nghiên cứu _toàn bộ_ tổng thể
Do không thể nghiên cứu toàn bộ tổng thể, ta thường chọn một _tập con_ của tổng thể, có số phần tử vừa đủ để khảo sát. Việc chọn tập con như thế được gọi là **phép lấy mẫu**. Tập con được lấy ra để khảo sát được gọi là một **mẫu**. Số phần tử trong mẫu, hay **kích thước mẫu** được kí hiệu là $n$.

Giả sử ta cần quan sát dấu hiệu $X$ trong tổng thể. Các giá trị thu được từ mẫu là ${x_1; x_2; ...; x_n}$.
Có nhiều cách để biểu diễn dữ liệu:
- Liệt kê dữ liệu
- Liệt kê dưới dạng bảng tần số: giả sử giá trị $x_i$ xuất hiện $n_i$ lần trong mẫu, ta có bảng sau:

| Giá trị | $a_1$ | $a_2$ | ... | $a_k$ |
| ------- | ----- | ----- | --- | ----- |
| Tần số  | $n_1$ | $n_2$ | ... | $n_k$ |
- Liệt kê dưới dạng khoảng: ta có thể nhóm các giá trị gần nhau thành các khoảng, và thể hiện từng khoảng với tần số của chúng trong bảng. Đối với mỗi khoảng, ta thường chọn giá trị chính giữa là giá trị đặc trưng, ví dụ với $(a_0;a_1]$ ta chọn $a_1' = \frac{a_0 + a_1}{2}$ là giá trị đặc trưng.

| Giá trị | $(a_0;a_1]$ | $(a_1;a_2]$ | ... | $(a_{k-1};x_k]$ |
| ------- | ----- | ----- | --- | ----- |
| Tần số  | $n_1$ | $n_2$ | ... | $n_k$ |
- Đối với hai dạng bảng trên, ta có thể sử dụng tần suất thay cho tần số.
- Ngoài ra dữ liệu còn có thể biểu diễn của biểu đồ,...

## Các đặc trưng của mẫu
Giả sử ta đã thu được mẫu $\{x_1; x_2;...;x_n\}$, mẫu này có các đặc trưng sau:
**Trung bình mẫu**: là tổng các giá trị của các phần tử trong mẫu chia cho kích thước mẫu
$$\bar{x} = \frac{\sum_{i=1}^n{x_i}}{n} = \frac{\sum_{i=1}^n{a_in_i}}{n}$$
**Trung vị mẫu**: là giá trị $\tilde{x}$ sao cho số giá trị trong mẫu lớn hơn hoặc bằng $\tilde{x}$ bằng số giá trị trong mẫu nhỏ hơn hoặc bằng $\tilde{x}$.
$$\tilde{x} = \begin{cases}
x_{(n+1)/2} \quad \text{ với n lẻ} \\
\frac{x_{n/2} + x_{n/2 + 1}}{2} \quad \text{ với n chẵn}
\end{cases}$$
**Mốt** là giá trị xuất hiện với tần số/tần suất lớn nhất trong mẫu
**Phương sai mẫu** là trung bình bình phương độ lệch giữa các giá trị mẫu với trung bình mẫu:
$$\hat{s}^2 = \frac{1}{n}\sum_{i=1}^n{(x_i - \bar{x})^2} = \frac{1}{n}\sum_{i=1}^n{n_i(a_i - \bar{x})^2}$$
Ta có công thức "tính nhanh" phương sai mẫu:
$$\hat{s}^2 = \frac{1}{n}\sum_{i=1}^n x_i^2 - n\bar{x}^2 = \frac{1}{n}\sum_{i=1}^n n_ia_i^2 - \bar{x}^2$$
**Độ lệch chuẩn mẫu** là căn bậc hai số học của phương sai mẫu, kí hiệu là $\hat{s}$
