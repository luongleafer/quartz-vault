---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 6
unit: 23
title: Luận điểm II của Maxwell
---
# Luận điểm thứ hai của Maxwell
## Phát biểu
- Mọi sự biến thiên của [[dien_truong|điện trường]] theo thời gian đều làm xuất hiện [[tu_truong|từ trường]] trong không gian
## Phân tích
 - Xét mạch gồm: [[dai_luong_dac_trung_dong_dien#Nguồn điện|nguồn điện]], [[tu_dien|tụ điện]], bóng đèn
 - Khi sử dụng nguồn điện một chiều, đèn không sáng. Dòng một chiều không đi qua tụ
 - Khi sử dụng nguồn điện xoay chiều, đèn sáng, có dòng điện tồn tại và đi qua điện môi giữa hai bản cực
 - Theo [[maxwell_I|luận điểm I]], để đảm bảo tính liên tục của mạch, ở mạch ngoài của tụ xuất hiện **dòng điện dẫn**, giữa hai bản cực xuất hiện **dòng điện dịch**, hai dòng điện này có cường độ như nhau
 - [[dai_luong_dac_trung_dong_dien#Vector mật độ dòng điện|Mật độ]] dòng điện dịch
$$J_{\text{dịch}} = \frac{i_{\text{dịch}}}{S} = \frac{i_{\text{dẫn}}}{S} = \frac{dq}{dt S} = \frac{\partial \sigma}{\partial t}$$
- Do $\sigma = E\epsilon_0\epsilon = D$ nên ta có
$$\vec{J}_{\text{dịch}} = \frac{\partial \vec{D}}{\partial t}$$

## Phương trình Maxwell-Ampere
- Theo [[tu_thong_dinh_luat_gauss#Định lí Ampere về dòng điện toàn phần|Định lí Ampere]], ta có

$$\oint_{(C)}{\vec{H}\vec{dl}} = \sum{I} = \int_{S}{\vec{J}\vec{dS}} = \int_{S}{(\vec{J_{\text{dẫn}}} + \frac{\partial D}{\partial t})\vec{dS}}$$

>[!formula] Phương trình Maxwell-Ampere
>Dạng tích phân
>$$\oint_{(C)}{\vec{H}\vec{dl}} = \int_{S}{(\vec{J_{\text{dẫn}}} + \frac{\partial \vec{D}}{\partial t})\vec{dS}}$$
>Dạng vi phân
>$$\nabla \times \vec{H} = \vec{J_{\text{dẫn}}} + \frac{\partial \vec{D}}{\partial t}$$
