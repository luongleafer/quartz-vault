---
tags:
  - note
  - university
subject: "[[it4110]]"
chapter: 0
unit: 1
title: Giới thiệu chung
---
# Giới thiệu
- **Tính toán khoa học** là tập hợp tất cả _công cụ_, _kỹ thuật_ và _lý thuyết_ cần thiết để phát triển và giải quyết các _mô hình toán học_ trong khoa học và kỹ thuật máy tính.
- Đặc điểm:
	- Sức mạnh máy tính
	- Phương pháp số
	- Bài toán kích thước lớn
- Cách tiếp cận: Bài toán (Problem) -> Mô hình (Model) -> Giải thuật (Algorithm) -> Kết quả (Result) -> Ứng dụng (Application)
- **Sai số (error)** là _khoảng cách_ giữa lời giải tìm được và lời giải toán học chính xác xuất hiện trong quá trình tính lời giải _gần đúng_.
- Nguồn gốc của sai số:
	- **Input data error**: sai số từ dữ liệu đầu vào.
	- **Model error**: sai số do mô hình xuất hiện khi lý tưởng hóa bài toán.
	- **Truncation error**: sai số rút gọn, xảy ra khi ngắt quá trình vô hạn.
	- **Round-off error**: sai số làm tròn, xuất hiện khi làm việc với số vô tỉ hoặc biểu diễn số trên máy tính.
- Các loại sai số:
	- $\hat{x}$ là xấp xỉ của $x$
	- **Sai số tuyệt đối**: $|\hat{x} - x|$
	- **Sai số tương đối**: $\frac{|\hat{x} - x|}{|x|}$ nếu $x \neq 0$
	- $\hat{x}$ chính xác đến $r$ chữ số sau dấu phẩy khi $$0.5 \times 10^{-r} < \frac{|\hat{x} - x|}{|x|} \le 5 \times 10^{-r}$$
- Điều kiện của bài toán:
	- **Well-conditioned** nếu sai số nhỏ trong dữ liệu dẫn đến sai số _nhỏ_ trong lời giải
	- **Ill-conditioned** nếu sai số nhỏ trong dữ liệu dẫn đên sai số _lớn_ trong lời giải
- Độ chính xác của máy tính
	- $fl(x)$ biểu diễn số thực dấu phẩy động, $\epsilon_M$ là độ chính xác, ta có $$\frac{|fl(x) - x|}{|x|} \le \epsilon_M$$
- **Sự ổn định số**: thuật toán _không ổn định_ nếu sai số làm tròn dẫn đến sai số _lớn_ trong kết quả
