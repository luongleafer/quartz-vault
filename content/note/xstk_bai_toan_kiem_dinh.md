---
tags:
  - note
  - university
subject: "[[mi2021]]"
chapter: 4
unit: 1
title: Bài toán kiểm định
---
# Kiểm định giả thuyết thống kê

## Giả thuyết - đối thuyết
**Giả thuyết thống kê** là bất cứ mệnh đề nào nói về tham số, dạng phân phối hay tính độc lập của các biến ngẫu nhiên.

Giả sử ta cần nghiên cứu tham số $\theta$ của một biến ngẫu nhiên $X$.
Giả thuyết $\theta = \theta_0$, với $\theta_0$ là một hằng số nào đó, được gọi là **giả thuyết không (null hypothesis)**. 

Giả thuyết trái với giả thuyết không được gọi là **đối thuyết**. Trong bài toán kiểm định, ta thường lập đối thuyết dựa trên giá trị của thống kê có được từ mẫu quan sát. Có 3 loại đối thuyết:
- $\theta \neq \theta_0$, còn gọi là đối thuyết hai phía
- $\theta < \theta_0$, còn gọi là đối thuyết bên trái
- $\theta > \theta_0$, còn gị là đối thuyết bên phải

Trong một bài toán kiểm định, ta xây dựng một cặp giả thuyết - đối thuyết $\{H_0; H_1\}$, dựa trên mẫu quan sát để quyết định có _bác bỏ_ $H_0$ (chấp nhận $H_1$) hoặc _chấp nhận_ $H_0$ (bác bỏ $H_1$). Quy tắc để đưa ra quyết định trên được gọi là **quy tắc kiểm định**.


## Sai lầm

Dựa theo quy tắc kiểm định và giá trị thống kê có được từ mẫu cụ thể, ta đưa ra quyết định. Khi này, có 4 trường hợp có thể xảy ra:

- Nếu ta bác bỏ $H_0$ và $H_0$ là sai, ta có quyết định đúng
- Nếu ta chấp nhận $H_0$ và $H_0$ là đúng, ta có quyết định đúng.
- Nếu ta bác bỏ $H_0$ và $H_0$ là đúng, ta có **sai lầm loại I** (false positive). Gọi xác suất để xảy ra sai lầm loại I là $\alpha$.
- Nếu ta chấp nhận $H_0$ và $H_0$ là sai, ta có **sai lầm loại II** (false negative). Gọi xác suất để xảy ra sai lầm loại II là $\beta$.

Bài toán kiểm định giả thuyết thường hướng tới _kiểm soát_ xác suất xảy ra sai lầm loại I $\alpha$ ở một mức nhỏ, cho trước, được gọi là **mức ý nghĩa**.

## Tiêu chuẩn kiểm định, miền bác bỏ
Để có quy tắc kiểm định, ta cần xây dựng **tiêu chuẩn kiểm định**. Theo đó, xây dựng mẫu ngẫu nhiên từ tổng thể cần khảo sát. Tiêu chuẩn kiểm định là một thống kê dựa trên mẫu ngẫu nhiên, sao cho thống kê này có _phân phối xác suất_ xác định khi $H_0$ là đúng. Gọi $\Omega$ là tiêu chuẩn kiểm định đang xét cho bài toán.

**Miền bác bỏ** là tập hợp $W_\alpha$ sao cho $P(\Omega \in W_\alpha)< \alpha$. Miền bác bỏ phụ thuộc vào phân phối xác suất của tiêu chuẩn kiểm định và mức ý nghĩa của bài toán. 
## Quy trình xây dựng quy tắc kiểm định

- Xác định cặp giả thuyết, đối thuyết dựa trên yêu cầu bài toán
- Đưa ra tiêu chuẩn kiểm định.
- Xác định miền bác bỏ
- Quy tắc kiểm định: nếu giá trị của tiêu chuẩn kiểm định nằm trong miền bác bỏ, ta tiến hành bác bỏ $H_0$. Ngược lại, ta không có đủ cơ sở để bác bỏ $H_0$.

