---
aliases: 
share: true
tags:
  - university
  - note
subject: "[[ph1120]]"
chapter: 3
unit: 12
title: Hiện tượng phân cực điện môi
---
# Hiện tượng phân cực điện môi

>[!definition] Điện môi
>- là những chất không dẫn điện
>- bên trong điện môi, điện tích sẽ định xứ 

## Hiện tượng

![[phan_cuc_dien_moi.excalidraw]]
- Khi đặt khối điện môi BC đồng chất, đẳng hướng trong [[dien_truong 1|điện trường]] của điện tích A, trên BC xuất hiện các **điện tích liên kết**
- Các điện tích liên kết định xứ trên BC, không tham gia chuyển động tự do
- Trường hợp BC không đồng chất và đẳng hướng, bên trong BC xuất hiện điện tích
- Các điện tích liên kết tạo ra điện trường $\overrightarrow{E'}$, khiến điện trường bên trong lòng chất điện môi thay đổi
$$\overrightarrow{E} = \overrightarrow{E_0} + \overrightarrow{E'}$$
Với $\overrightarrow{E_0}$ là điện trường ngoài do A

- Xét hai loại vật liệu điện môi có phân tử phân cực hoặc không phân cực

| Đặc điểm                      | Phân tử phân cực                                                | Phân tử không phân cực                                                                                                            |
| ----------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Phân bố electron              | không đối xứng xung quanh hạt nhân                              | đối xứng xung quanh hạt nhân                                                                                                      |
| Trước khi đưa vào điện trường | là lưỡng cực điện                                               | không là lưỡng cực điện                                                                                                           |
| Sau khi đưa vào điện trường   | $\overrightarrow{p_e}$ không bị $\overrightarrow{E_0}$ thay đổi | trở thành lưỡng cực điện<br>$\overrightarrow{p_e} =   \epsilon_0\alpha\overrightarrow{E_0}$ ($\alpha$ là độ phân cực của phân tử) |

## Vector phân cực điện môi
>[!definition] Định nghĩa
>- là tổng các vector lưỡng cực điện có trong một đơn vị thể tích của khối điện môi
>$$\overrightarrow{P_e} = \frac{\sum{\overrightarrow{p_{ei}}}}{\Delta V}$$

- Đối với điện môi có phân tử không phân cực, đặt trong điện trường đều, $\overrightarrow{p_{ei}}$ là không đổi và bằng $\overrightarrow{p_e}$ từ đó ta có
$$\overrightarrow{P_e} = \frac{n.\overrightarrow{p_e}}{\Delta V} = n_0.\overrightarrow{p_e} = n_0\alpha\epsilon_0\overrightarrow{E}$$
($n_0$ là mật độ phân tử, tức là số phân tử trong một đơn vị thể tích)
- Đặt $\chi_e = n_0.\alpha$, đại lượng này được gọi là **độ cảm điện môi**, không có thứ nguyên, không phụ thuộc vào $\overrightarrow{E}$, ta có

>[!formula] Vector phân cực điện môi đối với phân tử không phân cực
>$$\overrightarrow{P_e} = \epsilon_0\chi_e\overrightarrow{E}$$

- Đối với điện môi có phân tử phân cực và điện trường ngoài yếu, công thức trên vẫn áp dụng, tuy nhiên
$$\chi _e = \frac{n_0p_e^2}{3\epsilon_0kT}$$
với $k$ là [Hằng số Boltzmann](https://vi.wikipedia.org/wiki/H%E1%BA%B1ng_s%E1%BB%91_Boltzmann) và $T$ là nhiệt độ tuyệt đối của khối điện môi

>[!formula] Vector phân cực điện đối với phân tử phân cực
>$$\overrightarrow{P_e} = \frac{n_0p_e^2}{3kT}\overrightarrow{E}$$

- Xét điện môi có dạng khối trụ xiên, đường sinh độ dài $L$, song song với $\overrightarrow{E}$ và $\overrightarrow{P_e}$, hai đáy song song, có diện tích $\Delta S$, vector pháp tuyến $\overrightarrow{n}$. Gọi $\alpha$ là góc giữa $\overrightarrow{E}$ và $\overrightarrow{n}$
- Mật độ điện mặt trên hai đáy là $\sigma'$
- Ta có $\sum{p_{ei}} = \sigma'\Delta S L$, $\Delta V = \Delta S L\cos\alpha$
- Từ đó ta có $P_e = \frac{\sum{p_{ei}}}{\Delta V} = \frac{\sigma'}{\cos\alpha}$ vậy $\sigma' = P_e\cos\alpha = P_{en}$ ($\overrightarrow{P_{en}}$ là hình chiếu của $\overrightarrow{P_e}$ lên $\overrightarrow{n}$ )

>[!formula] Mối liên hệ giữa mật độ điện tích liên kết và vector phân cực điện môi
>$$\sigma' = P_{en}$$
>Mật độ điện tích liên kết về giá trị bằng hình chiếu của vector phân cực điện môi lên vector pháp tuyến của mặt giới hạn
>

