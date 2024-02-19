## [[Computer Science]]
![[cs50Week0Slide38.png]]
- **Input và Output:** [[Máy tính]] lấy dữ liệu ([[input]]) ➡️ và tạo ra kết quả ([[output]]). Quá trình nội bộ giữa các giai đoạn này là trọng tâm của khoa học máy tính.

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
## [[Algorithms]]

Thuật toán là cách giải quyết vấn đề trong khoa học máy tính và lập trình. Ví dụ, để tìm một tên cụ thể trong quyển danh bạ điện thoại:
- Cách 1 - Đọc từng trang, từ trang đầu tiên đến trang cuối cùng để tìm - O(*n*).
- Cách 2 - Đọc từng cặp trang - O(*n/2*).
- Cách 3 - Chia đôi danh bạ, kiểm tra tên ở nửa nào và tiếp tục lặp lại cho đến khi tìm ra - O(log2 _n_)

![[cs50Week0Slide141 1.png]]
Trong đó hiệu quả của thuật toán được đo bằng ký hiệu O:
- O(*n*) - Số bước tăng theo số phần tử (n).
- O(*n/2*) - Só bước giảm một nửa so với O(*n*) khi n tăng gấp đôi.
- O(log2 _n_) - Số bước tăng ít kể cả khi n tăng gấp đôi.
## [[Pseudocode]]

Mã giả là phiên bản code dễ đọc gần với ngôn ngữ giao tiếp thường ngày. Ví dụ, với thuật toán thứ 3 ở trên

```
1  Pick up phone book
2  Open to middle of phone book
3  Look at page
4  If person is on page
5      Call person
6  Else if person is earlier in book
7      Open to middle of left half of book
8      Go back to line 3
9  Else if person is later in book
10     Open to middle of right half of book
11     Go back to line 3
12 Else
13     Quit
```

- Viết mã giả trước khi viết code chính thức giúp suy nghĩ về logic của vấn đề.
- Có thể cung cấp thông tin cho những người khác để hiểu về quyết định cũng như cách thức hoạt động của code.
- Một số đặc điểm cần lưu ý trong **pseudocode** ở ví dụ:
	- Đầu tiên, một số dòng bắt đầu với các động từ `Pick up`, `Open`, `Look at` là các hàm - **function**.
	- Thứ hai, các dòng bao gồm câu lệnh như `if` hoặc `else if` là các điều kiện - **conditional**.
	- Thứ ba, chú ý các câu có thể được biểu thị là `true` hoặc `false`, chẳng hạn như `person is earlier in the book` gọi là các biểu thức **boolean**.
## [[Artificial Intelligence]]

Có thể xây dựng AI bằng các block cơ bản như:
```
If student says hello
    Say hello back
Else if student says goodbye
    Say goodbye back
Else if student asks how you are
    Say you're well
Else if student asks why 111 in binary is 7 in decimal
...
```
Để ý rằng chỉ với một vài tương tác nhỏ, chúng ta đã cần tới nhiều dòng code. Vậy với hàng ngàn, hàng chục ngàn tương tác tiềm năng, chúng ta sẽ cần phải có bao nhiều dòng code?
Các **mô hình ngôn ngữ lớn** - [[Large Language Models (LLMs)]] sẽ phân tích các mẫu trong khối lượng lớn văn bản. Chúng cố gắng dự đoán từ nào sẽ xuất hiện tiếp theo hoặc được sử dụng cùng nhau.
![[cs50Week0Slide42.png]]