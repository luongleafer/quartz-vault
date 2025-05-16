---
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 4
unit: 5
title: Biểu diễn đồ thị
published: 2025-04-21
---

# Biểu diễn đồ thị
- 2 vấn đề cần quan tâm:
	- Bộ nhớ đòi hỏi
	- Thời gian trả lời truy vấn thường xuyên
## Ma trận kề
- $|V| \times |V|$ ma trận A
- Các đỉnh được đánh số từ 1 đến $|V|$ theo thứ tự nào đó
- $A[i,j] = a_{ij} = \begin{cases}1 \,\,\, \text{nếu} (i;j) \in E\\0 \,\,\, \text{nếu} (i;j) \notin E\end{cases}$
- Ví dụ:
![[Pasted image 20250421075302.png]]
![[Pasted image 20250421075553.png]]
![[Pasted image 20250421075640.png]]
![[Pasted image 20250421075905.png]]
- Tính chất:
	- Với đồ thị vô hướng có ma trận kề A thì:
		- A đối xứng
		- Bậc của đỉnh v là tổng các phần tử trên dòng v
- Bộ nhớ:
	- $|V|^2$ bits
	- $(|V|^2+|V|)/2$ với đồ thị vô hướng, khó cài đặt
	- 
- Thời gian
	- Hai đỉnh $i$ và $j$ có kề nhau? $O(1)$
	- Bổ sung/loại bỏ cạnh? $O(1)$
	- Bổ sung đỉnh? Tăng kích thước ma trận
	- Liệt kê các đỉnh kề v? $O(|V|)$
![[Pasted image 20250421081459.png]]
![[Pasted image 20250421082220.png]]
![[Pasted image 20250421082425.png]]
![[Pasted image 20250421082842.png]]
![[Pasted image 20250421083726.png]]
![[Pasted image 20250421083845.png]]
![[Pasted image 20250421084044.png]]
![[Pasted image 20250421085058.png]]