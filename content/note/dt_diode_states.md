---
aliases:
share: false
tags:
  - university
  - note
subject: "[[it3420]]"
chapter: 2
unit: 2
title: Trạng thái của diode
---
# Trạng thái của Diode
## Trạng thái cân bằng nhiệt
- Khi đặt hai lớp bán dẫn n và p tiếp xúc nhau, do chênh lệch nồng độ, xảy ra hiện tượng _khuếch tán_:
	- Electron: n sang p
	- Lỗ trống: p sang n
- Khi khuếch tán, điện tích trái dấu gặp nhau, tạo một _vùng hẹp_ ở ranh giới. Ở vùng này, nồng độ hạt dẫn _rất thấp_, gọi là **vùng nghèo**.

## Trạng thái phân cực ngược
- Khi ta đặt điện áp dương $V_R$ vào đầu n:
	- electron sẽ được đưa thêm vào đầu p
	- lỗ trống được đưa vào đầu n
	- làm _rộng thêm_ vùng nghèo
	- lúc này, dòng điện, mặc dù có, chỉ là dòng chuyển dời của các hạt dẫn thiểu số, với cường độ rất nhỏ và nhanh chóng đạt trạng thái bão hòa
## Trạng thái phân cực thuận
- Khi đặt điện áp dương $V_D$ vào đầu p:
	- electron được đưa vào đầu n
	- lỗ trống được đưa vào đầu p
	- vùng nghèo bị _thu hẹp_ dần
	- gây ra dòng hạt dẫn đa số chạy qua ranh giới giữa hai lớp bán dẫn
	- càng tăng điện áp, vùng nghèo càng mỏng dần, dẫn tới dòng điện càng lớn
	- trạng thái này được gọi là **phân cực thuận**

>[!formula] Dòng điện qua diode
>$$I_D = I_S(e^\frac{V_D}{nV_T} - 1)$$
>Trong đó:
>$I_S$ là dòng bão hòa phân cực ngược, trong khoảng $10^{-18}$ đến $10^{-12}$ (A)
>$V_T$ là điện áp nhiệt, ở nhiệt độ phòng là $0,026 (V)$
>$n$ là hệ số lý tưởng, trong đoạn $[1;2]$

### Điện áp đánh thủng
- Khi ta tăng điện áp phân cực ngược đến một giá trị đủ lớn, dòng điện ngược _tăng vọt_, dẫn đến diode bị _đánh thủng_