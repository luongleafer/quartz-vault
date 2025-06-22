---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 2
unit: 9
title: Hiện tượng điện hưởng
---

# Hiện tượng điện hưởng

## Mô tả hiện tượng
- Khi đặt một [[vat_dan|vật dẫn cân bằng tĩnh điện]] trong một [[dien_truong 1|điện trường]], dưới tác dụng của điện trường làm cho các điện tích di chuyển, xuất hiện **điện tích cảm ứng**

>[!definition] Hiện tượng điện hưởng
>Là hiện tượng xuất hiện các điện tích cảm ứng trên vật dẫn (lúc đầu không mang điện) khi đặt trong điện trường
## Định lí phần tử tương đương
![[dien_huong.excalidraw]]
- Xét các đường cảm ứng từ tựa trên một phần $\Delta S_1$ của $A$ và tới tận cùng là $\Delta S_2$ của $BC$. Dựng mặt Gauss hợp bởi các đường cảm ứng điện và $\Delta S_1$ và $\Delta S_2$
- Điện thông gửi qua mặt Gauss
$$\phi = \oint_{S}{\overrightarrow{D}\,\overrightarrow{dS}} = \oint_{\Delta S_1}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{\Delta S_2}{\overrightarrow{D}\,\overrightarrow{dS}} + \oint_{S_{xq}}{\overrightarrow{D}\,\overrightarrow{dS}}$$
- Trên $\Delta S_1$ và $\Delta S_2$, do điện trường trong bằng 0, nên điện thông gửi qua hai mặt này bằng 0
- Trên $S_{xq}$, do $\overrightarrow{D}$ luôn vuông góc với $\overrightarrow{n}$ nên điện thông = 0
- Vậy ta có $\phi = 0$
- Áp dụng [[ostrogradsky-gauss|Định lí OG]] ta có $\phi = \Delta q_1 + \Delta q_2 = 0$

>[!formula] Định lí phần tử tương đương
>Điện tích tương ứng trên các phần tử tương đương có cùng độ lớn nhưng trái dấu
>$$\Delta q_1 + \Delta q_2 = 0$$

## Điện hưởng một phần và điện hưởng toàn phần
- Gọi điện tích của vật mang điện A là $q$, độ lớn điện tích cảm ứng của $BC$ do hiện tượng điện hưởng là $q'$
- Trường hợp các đường sức điện từ A, một phần kết thúc ở BC, phần còn lại tiến đến vô cùng, ta có $q' < q$, đây là **hiện tượng điện hưởng một phần**
![[dien_huong.excalidraw]]
- Trường hợp tất cả các đường sức điện từ A đều kết thúc ở BC, ta có $q' = q$, đây là **hiện tượng điện hưởng toàn phần**, ví dụ như hình dưới
![[dien_huong_toan_phan.excalidraw]]

