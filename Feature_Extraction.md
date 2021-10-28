# **Trích xuất đặc trưng là gì?**
Trích xuất đặc trưng là một phần của quy trình giảm kích thước, trong đó, tập hợp dữ liệu thô ban đầu được chia và giảm thành các nhóm dễ quản lý hơn. Vì vậy, khi chúng ta muốn xử lý sẽ dễ dàng hơn. Đặc điểm quan trọng nhất của các tập dữ liệu lớn này là chúng có một số lượng lớn các biến. Các biến này yêu cầu nhiều tài nguyên máy tính để xử lý chúng. Vì vậy, việc trích xuất đặc trưng giúp có được những tính năng tốt nhất từ các tập dữ liệu lớn đó bằng cách chọn và kết hợp các biến thành các tính năng, do đó, giảm lượng dữ liệu một cách hiệu quả. Các tính năng này rất dễ xử lý, nhưng vẫn có thể mô tả tập dữ liệu thực tế với độ chính xác và độc đáo.
# **Tại sao trích xuất đặc trưng hữu ích?**
Kỹ thuật trích xuất các tính năng rất hữu ích khi chúng ta có một tập dữ liệu lớn và cần giảm số lượng tài nguyên mà không làm mất bất kỳ thông tin quan trọng hoặc liên quan nào. Tính năng trích xuất giúp giảm lượng dữ liệu dư thừa từ tập dữ liệu.

Cuối cùng, việc giảm dữ liệu sẽ giúp xây dựng mô hình với ít nỗ lực của máy hơn và cũng tăng tốc độ học và các bước tổng quát hóa trong quá trình máy học.
# **Làm thế nào để máy tính lưu trữ hình ảnh?**
Điều đầu tiên, chúng ta cần hiểu cách một máy có thể đọc và lưu trữ hình ảnh. Việc tải ảnh, đọc chúng rồi xử lý qua máy rất khó vì máy không có mắt như chúng ta.

Máy móc nhìn thấy bất kỳ hình ảnh nào dưới dạng ma trận số. Kích thước của ma trận này thực sự phụ thuộc vào số lượng pixel của hình ảnh đầu vào.

**_Pixel là gì?_**

Giá trị Pixel cho mỗi pixel là viết tắt hoặc mô tả độ sáng và màu sắc của pixel đó. Vì vậy, trong trường hợp đơn giản nhất của ảnh nhị phân, giá trị pixel là số 1 bit cho biết nền trước hoặc nền sau (ảnh trắng đen). Vậy pixel là số hoặc giá trị biểu thị cường độ hoặc độ sáng của pixel. Các số nhỏ gần 0 biểu thị màu đen và các số lớn gần 255 biểu thị màu trắng. Vậy, đây là khái niệm về pixel và cách máy nhìn thấy hình ảnh thông qua các con số mà không cần mắt.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-16.png)

Tuy nhiên, đối với trường hợp hình ảnh có màu, chúng ta có 3 ma trận hoặc 3 kênh: màu đỏ (R), màu xanh lá (G), xanh lam (B). Trong 3 ma trận này, mỗi ma trận có các giá trị từ 0-255 đại diện cho cường độ màu của pixel đó.

![MATLAB | RGB image representation - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/Pixel.jpg)

Có thể thấy chúng ta cũng có 3 ma trận đại diện cho kênh RGB. Ba kênh này được xếp chồng lên nhau và được sử dụng để tạo thành một hình ảnh có màu. Đây là cách máy tính có thể phân biệt giữa các hình ảnh.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-41.png)

![](https://scontent.fdad1-2.fna.fbcdn.net/v/t1.6435-9/247005982_190644936546824_6207417727032389072_n.jpg?_nc_cat=102&ccb=1-5&_nc_sid=0debeb&_nc_ohc=oPcag37aOTYAX9yTFYE&_nc_ht=scontent.fdad1-2.fna&oh=a5bff9ead5260227c9f25cef4346d041&oe=619EEAB0)

![](https://scontent.fdad2-1.fna.fbcdn.net/v/t1.6435-9/246933504_190644979880153_3019617350402214686_n.jpg?_nc_cat=107&ccb=1-5&_nc_sid=0debeb&_nc_ohc=clUTel-RbPMAX__T0RV&_nc_ht=scontent.fdad2-1.fna&oh=eaad459f22aadd147ab956a068dd33c2&oe=61A02E05)



# **Cách sử dụng kỹ thuật trích xuất đặc trưng cho dữ liệu hình ảnh**
## **1. Các đặc trưng dưới dạng giá trị pixel trong ảnh xám**
Nếu chúng ta sử dụng ví dụ tương tự như hình ảnh mà chúng ta sử dụng ở trên tthì kích thước của hình ảnh là 340 x 680. Số lượng các đặc trưng giống như số lượng pixel nên số lượng đặc trưng sẽ là 340 x 680 = 231200.

Vì vậy, làm cách nào để khai báo 231200 pixel là các đặc trưng của hình ảnh này? Giải pháp là, chúng ta chỉ cần nối từng giá trị pixel lần lượt để tạo ra một vectơ đặc trưng cho hình ảnh.

`	`![](https://scontent.fdad1-1.fna.fbcdn.net/v/t1.6435-9/248351355_190644929880158_2865498114925000134_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=0debeb&_nc_ohc=OBRIE97LiaMAX9nrKl1&_nc_ht=scontent.fdad1-1.fna&oh=5d4c0ead0c536987d776fa3d9628db59&oe=619FF8F1)
## **2. Các đặc trưng là giá trị pixel trung bình các kênh trong ảnh RGB**

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-6.png)

![](https://scontent.fdad1-1.fna.fbcdn.net/v/t1.6435-9/248439750_190644896546828_1527624821140439700_n.jpg?_nc_cat=103&ccb=1-5&_nc_sid=0debeb&_nc_ohc=tBBiZloB9t0AX8y1Td_&_nc_ht=scontent.fdad1-1.fna&oh=27be856a319765dd40f9bb8fb3febcbc&oe=61A087AE)

Đối với trường hợp này, hình ảnh có một kích thước (340, 680, 3). Ba giá trị này đại diện cho giá trị RGB cũng như số lượng kênh. Bây giờ chúng ta sẽ sử dụng phương pháp trước để tạo các đặc trưng.

Tổng số đặc trưng của trường hợp này là 340\*680\*3 = 693600

![](https://scontent.fdad2-1.fna.fbcdn.net/v/t1.6435-9/247125801_190645003213484_2685084462417721596_n.jpg?_nc_cat=101&ccb=1-5&_nc_sid=0debeb&_nc_ohc=ELxRcK-VbOsAX_lSTyF&_nc_ht=scontent.fdad2-1.fna&oh=1ee33e0006ac7c46fff56906ddd1c51c&oe=61A023FF)

Trong hình ảnh màu này có một ma trận 3D có kích thước (340 \* 680 \* 3) trong đó 340 biểu thị chiều cao, 680 là chiều rộng và 3 là số kênh. Để có được giá trị pixel trung bình cho hình ảnh, chúng ta sẽ sử dụng vòng lặp for.

![](https://scontent.fdad1-2.fna.fbcdn.net/v/t1.6435-9/248417457_190645039880147_1364748352007627007_n.jpg?_nc_cat=102&ccb=1-5&_nc_sid=0debeb&_nc_ohc=yH-khG8W7i0AX82K8d3&_nc_ht=scontent.fdad1-2.fna&oh=261380b00036b201e215a207ce48cf76&oe=619E6B7B)

Bây giờ chúng ta đã tạo ra một ma trận mới có cùng chiều cao và chiều rộng nhưng chỉ có 1 kênh. Để chuyển đổi ma trận thành mảng 1 chiều, chúng ta sẽ sử dụng thư viện Numpy như phần trước.

![](https://scontent.fdad1-3.fna.fbcdn.net/v/t1.6435-9/246377635_190645046546813_8398213391397648257_n.jpg?_nc_cat=110&ccb=1-5&_nc_sid=0debeb&_nc_ohc=oEJBd3Ku5rwAX82lzJw&_nc_ht=scontent.fdad1-3.fna&oh=a98a9d63f6adfec2503c9d1b16e9a825&oe=61A1A376)

## **3. Các đặc trưng dưới dạng cạnh**
Cạnh về cơ bản là nơi có sự thay đổi rõ nét về màu sắc. Và như chúng ta đã biết, một hình ảnh được biểu diễn dưới dạng các con số. Vì vậy, chúng tôi sẽ tìm kiếm các pixel xung quanh có sự thay đổi mạnh mẽ trong các giá trị pixel.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-81.png)

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-9.png)

Để xác định xem một pixel có phải là một cạnh hay không, chúng ta chỉ cần trừ các giá trị ở hai bên của pixel. Đối với ví dụ này, ta có giá trị được đánh dấu là 85. Chúng ta sẽ tìm sự khác biệt giữa hai giá trị 89 và 78. Vì sự khác biệt này không lớn lắm nên ta có thể nói rằng không có cạnh xung quanh pixel này.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-101.png)

Bây giờ hãy xem xét pixel 125 được đánh dấu trong hình. Vì sự khác biệt giữa các giá trị ở hai bên của pixel này lớn, ta có thể kết luận rằng có một sự chuyển đổi đáng kể tại pixel này và do đó nó là một cạnh. Bây giờ câu hỏi đặt ra là liệu chúng ta có cần phải thực hiện bước này theo cách thủ công không?
Câu trả là không. Có nhiều nhân khác nhau có thể được sử dụng để làm nổi bật các cạnh trong hình ảnh. Phương pháp chúng ta vừa thảo luận cũng có thể đạt được bằng cách sử dụng nhân Prewitt (theo hướng x). Dưới đây là nhân Prewitt:

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-132.png)

Lấy các giá trị xung quanh pixel đã chọn và nhân nó với nhân đã chọn (nhân Prewitt). Sau đó, chúng ta có thể thêm các giá trị kết quả để nhận được giá trị cuối cùng. Vì chúng ta đã có -1 trong một cột và 1 trong cột kia, nên việc thêm các giá trị tương đương với việc lấy chênh lệch.


![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-111.png)

Có rất nhiều loại nhân dưới đây là 4 loại hạt nhân thường được sử dụng phổ biến nhất:

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-121.png)

![](https://scontent.fdad1-3.fna.fbcdn.net/v/t1.6435-9/247413980_190645079880143_4882805522114784878_n.jpg?_nc_cat=110&ccb=1-5&_nc_sid=0debeb&_nc_ohc=ylWcMinPTW0AX9HsAJq&_nc_ht=scontent.fdad1-3.fna&oh=a20b3e8b50a8e5efb5549bc773b16a9d&oe=619F8CE6)

![](https://scontent.fdad2-1.fna.fbcdn.net/v/t1.6435-9/249939010_190645106546807_9141650186866608310_n.jpg?_nc_cat=108&ccb=1-5&_nc_sid=0debeb&_nc_ohc=zWAhM9rU66cAX8hyDSp&_nc_ht=scontent.fdad2-1.fna&oh=a30c114d815ee2a6adfb5f59b7d7ea7e&oe=619E3F7C)

# **Lời kết**
Chúng ta đã đi tìm hiểu những khái niệm cơ bản đầu tiên liên quan đến trích xuất đặc trưng. Trong bài viết này trình bày 3 cách cơ bản để trích xuất đặc trưng đó là:
  1. Các đặc trưng dưới dạng giá trị pixel trong ảnh xám
  2. Các đặc trưng là giá trị pixel trung bình các kênh trong ảnh RGB
  3. Các đặc trưng dưới dạng cạnh

## **Authors**

* **Truong Bao Nguyen** - [truongbaonguyen](https://github.com/truongbaonguyen)

* **Trinh Tran Trung** - [flyingman2401](https://github.com/flyingman2401)

## **License**
