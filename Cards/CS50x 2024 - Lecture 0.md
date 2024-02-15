## [[Computer Science]] - Khoa học máy tính
![[cs50Week0Slide38.png]]
- **Input và Output:** Máy tính lấy dữ liệu ([[input]]) ➡️ và tạo ra kết quả ([[output]]). Quá trình nội bộ giữa các giai đoạn này là trọng tâm của khoa học máy tính.

- **Binary System:** Không giống như con người sử dụng hệ thập phân ([[unary]]) (cơ số 10), máy tính sử dụng hệ nhị phân ([[binary]]) (cơ số 2). Điều này có nghĩa là chúng chỉ sử dụng 0 và 1 để biểu diễn thông tin.

- **Bit và Byte:** Một bit là một chữ số nhị phân đơn (0 hoặc 1). Tám [[bit]] tạo thành một [[byte]], có thể biểu diễn các số từ [[0-255]].

## [[ASCII]]
![[cs50Week0Slide93.png]]
- Chữ cái được biểu diễn bằng các cặp nhị phân 1 và 0 giống như số.
- Tiêu chuẩn ASCII ánh xạ các chữ cái cụ thể với các số cụ thể. 
	  *(Ví dụ: A = 65 = 01000001)*
- Mã ASCII giúp thống nhất cách biểu diễn văn bản trên máy tính.
- Giới hạn số lượng ký tự được biểu diễn (255). Các ngôn ngữ với ký tự đặc biệt cần sử dụng bảng mã khác.
## [[Unicode]]
![[cs50Week0Slide103.png]]
- Với sự phát triển của giao tiếp trực tuyến, cần một cách thể hiện văn bản đa dạng hơn hệ thống nhị phân có hạn.
- Chuẩn **Unicode** mở rộng số bit để máy tính truyền tải và hiểu nhiều ký tự hơn, bao gồm ký tự đặc biệt và cả biểu tượng cảm xúc ([[emoji]]).
- **Ví dụ:**
	- (U+1F44D): Ngón cái giơ lên mặc định.
	- (U+1F44D U+1F3FD): Ngón cái giơ lên tông da tối.
## [[Representation]]

- Màu sắc có thể được biểu diễn bằng các số 0 và 1.
- Đỏ, Xanh lá cây, Xanh dương ([[RGB]]) là sự kết hợp của ba số.
	![[cs50Week0Slide118.png]]
	*72, 73, 33 tương ứng với chữ "HI!" trong văn bản, nhưng sẽ được trình bày là màu vàng nhạt trong hình ảnh vì giá trị đỏ là 72, xanh lá cây là 73 và xanh dương là 33.*

- Số nhị phân cũng có thể biểu diễn hình ảnh, video và âm nhạc:
    - Hình ảnh là tập hợp các giá trị RGB.
    - Video là chuỗi nhiều hình ảnh được lưu trữ cùng nhau, giống như flipbook.
    - Âm nhạc có thể được biểu diễn thông qua dữ liệu [[MIDI]].