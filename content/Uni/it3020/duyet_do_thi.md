---
tags:
  - university
  - note
subject: "[[it3020]]"
chapter: 5
unit: 9
title: Duyệt đồ thị
---
## Phương pháp duyệt theo chiều rộng (Breadth-First Search - BFS)
- Thuật toán:
	- Khởi tạo hàng đợi rỗng $Q$
	- Thêm đỉnh nguồn vào $Q$, đặt là `đã thăm`
	- Lặp cho đến khi $Q$ rỗng:
		- Lấy đỉnh $q$ khỏi $Q$
		- Thao tác với đỉnh $q$
		- Thêm các đỉnh kề với $q$ mà chưa được thăm vào $Q$, đánh dấu các đỉnh là `đã thăm`
- Độ phức tạp: $O(|V|+|E|)$, trong đó
	- Khởi tạo: $O(|V|)$
	- Khi làm việc với hàng đợi, ta đưa các đỉnh lần lượt vào và ra khỏi hàng đợi, nên thời gian là $O(|V|)$
	- Khi làm việc với danh sách kề để lấy đỉnh cho vào hàng đợi, ta duyệt qua tất cả các đỉnh, thời gian là $O(|E|)$
- Cây BFS: là đồ thị con của $G$ có được khi thực hiện BFS
- Việc thực hiện BFS sẽ thăm đỉnh $t$ với đường đi ngắn nhất _về số cạnh_
## Phương pháp duyệt theo chiều sâu (Depth-First Search - DFS)
- Thuật toán:
	- Đặt tất cả các đỉnh là `chưa thăm`
	- Từ đỉnh đầu tiên:
		- Đặt đỉnh hiện tại là `đã thăm`
		- Thao tác với đỉnh hiện tại
		- Duyệt DFS với tất cả các đỉnh kề với nó
- Thời gian bắt đầu và kết thúc duyệt
	- Xét biến $t$, bắt đầu bằng 0
	- Mỗi lần thăm một đỉnh $v$, tăng $t$ lên 1, đặt $d[v] = t$
	- Khi đã thăm hết các đỉnh kề với $v$, tăng $t$ lên 1, đặt $f[v] = t$
- Bổ đề các khoảng cách lồng nhau: Trong quá trình duyệt DFS:
	- $u$ là đỉnh con của $v$ nếu đoạn $[d[u];f[u]]$ nằm trong đoạn $[d[v];f[v]]$
	- $u$ là đỉnh tổ tiên của $v$ nếu đoạn $[d[u];f[u]]$ chứa đoạn $[d[v];f[v]]$
	- Nếu hai đoạn trên rời nhau, ta gọi $u$ và $v$ là hai đỉnh không có quan hệ họ hàng
- Phân loại cạnh:
	- Cạnh cây là cạnh đi từ tổ tiên đến đỉnh con đầu tiên của nó
	- Cạnh tới là cạnh đi từ tổ tiên đến con cháu, khác cạnh cây
	- Cạnh ngược là cạnh đi từ con cháu đến tổ tiên
	- Cạnh vòng là cạnh kề với hai đỉnh không có quan hệ họ hàng
## Ứng dụng của DFS và BFS
- Kiểm tra tính liên thông:
	- Nếu ta duyệt DFS/BFS đến khi tất cả các đỉnh đều được thăm, mỗi lần một đỉnh được gọi DFS và BFS để bắt đầu duyệt, ta có một thành phần liên thông
- Tìm [[khai_niem_do_thi#Đường đi|đường đi]]
- Phát hiện chu trình:
	- Đồ thị không có chu trình nếu và chỉ nếu việc duyệt DFS không phát hiện cạnh ngược
- Xét tính liên thông mạnh:
	- Từ một đỉnh $u$ nào đó, duyệt DFS, nếu có đỉnh chưa được duyệt, đồ thị không liên thông
	- Đảo ngược hướng tất cả các cạnh trên đồ thị, lặp lại bước trên
	- Nếu qua hai bước đều không tìm thấy đỉnh chưa được duyệt, ta có đồ thị liên thông mạnh
- Định hướng đồ thị:
	- Xét đồ thị vô hướng $G$ liên thông
	- Duyệt DFS trên $G$, phân loại cạnh và chọn ra cạnh cây, cạnh tới và cạnh ngược, lập thành đồ thị con $G(\sigma)$ . 
	- $G$ định hướng được nếu $G(\sigma)$ liên thông mạnh
