# **CÁC THUẬT TOÁN MACHINE LEARNING**

## **I. Phân nhóm thuật toán dựa trên phương thức học**

Theo phương thức học, các thuật toán Machine Learning thường được chia làm 4 nhóm: Supervised learning, Unsupervised learning, Semi-supervised learning và Reinforcement learning. Có một số cách phân nhóm không có Semi-supervised learning hoặc Reinforcement learning.

### **1. Supervised Learning (Học có giám sát)**

Supervised learning là thuật toán dự đoán đầu ra (outcome) của một dữ liệu mới (new input) dựa trên các cặp (input, outcome) đã biết từ trước. Cặp dữ liệu này còn được gọi là (data, label), tức (dữ liệu, nhãn). Supervised learning là nhóm phổ biến nhất trong các thuật toán Machine Learning.

*Ví dụ:* Trong nhận dạng chữ viết tay, ta có ảnh của hàng nghìn ví dụ của mỗi chữ số được viết bởi nhiều người khác nhau. Chúng ta đưa các bức ảnh này vào trong một thuật toán và chỉ cho nó biết mỗi bức ảnh tương ứng với chữ số nào. Sau khi thuật toán tạo ra một mô hình, tức một hàm số mà đầu vào là một bức ảnh và đầu ra là một chữ số, khi nhận được một bức ảnh mới mà mô hình chưa nhìn thấy bao giờ, nó sẽ dự đoán bức ảnh đó chứa chữ số nào.

![image](https://user-images.githubusercontent.com/87793139/149309426-ad60d750-02fa-41fd-97de-fc0816be4e90.png)

Thuật toán supervised learning còn được tiếp tục chia nhỏ ra thành hai loại chính:

#### **Classification (Phân loại)**

Một bài toán được gọi là classification nếu các label của input data được chia thành một số hữu hạn nhóm. Ví dụ: Gmail xác định xem một email có phải là spam hay không; các hãng tín dụng xác định xem một khách hàng có khả năng thanh toán nợ hay không. 

#### **Regression (Hồi quy)**

Nếu label không được chia thành các nhóm mà là một giá trị thực cụ thể. Ví dụ: một căn nhà rộng x m2, có y phòng ngủ và cách trung tâm thành phố z km sẽ có giá là bao nhiêu?

### **2. Unsupervised Learning (Học không giám sát)**

Trong thuật toán này, chúng ta không biết được outcome hay nhãn mà chỉ có dữ liệu đầu vào. Thuật toán unsupervised learning sẽ dựa vào cấu trúc của dữ liệu để thực hiện một công việc nào đó, ví dụ như phân nhóm (clustering) hoặc giảm số chiều của dữ liệu (dimension reduction) để thuận tiện trong việc lưu trữ và tính toán. Những thuật toán loại này được gọi là Unsupervised learning vì không giống như Supervised learning, chúng ta không biết câu trả lời chính xác cho mỗi dữ liệu đầu vào.

Các bài toán Unsupervised learning được tiếp tục chia nhỏ thành hai loại:

#### **Clustering (phân nhóm)**

Một bài toán phân nhóm toàn bộ dữ liệu X thành các nhóm nhỏ dựa trên sự liên quan giữa các dữ liệu trong mỗi nhóm. Ví dụ: phân nhóm khách hàng dựa trên hành vi mua hàng. Điều này cũng giống như việc ta đưa cho một đứa trẻ rất nhiều mảnh ghép với các hình thù và màu sắc khác nhau, ví dụ tam giác, vuông, tròn với màu xanh và đỏ, sau đó yêu cầu trẻ phân chúng thành từng nhóm. Mặc dù không cho trẻ biết mảnh nào tương ứng với hình nào hoặc màu nào, nhiều khả năng chúng vẫn có thể phân loại các mảnh ghép theo màu hoặc hình dạng.

![image](https://user-images.githubusercontent.com/87793139/149309570-4eb12e83-b52e-4139-86a4-721dc47dbcd5.png)

#### **Association**

Là bài toán khi chúng ta muốn khám phá ra một quy luật dựa trên nhiều dữ liệu cho trước. Ví dụ: những khách hàng nam mua quần áo thường có xu hướng mua thêm đồng hồ hoặc thắt lưng; những khán giả xem phim Spider Man thường có xu hướng xem thêm phim Bat Man, dựa vào đó tạo ra một hệ thống gợi ý khách hàng (Recommendation System), thúc đẩy nhu cầu mua sắm.

### 3. **Semi-Supervised Learning (Học bán giám sát)**

Các bài toán khi chúng ta có một lượng lớn dữ liệu X nhưng chỉ một phần trong chúng được gán nhãn được gọi là Semi-Supervised Learning. Những bài toán thuộc nhóm này nằm giữa hai nhóm được nêu bên trên.

Một ví dụ điển hình của nhóm này là chỉ có một phần ảnh hoặc văn bản được gán nhãn (ví dụ bức ảnh về người, động vật hoặc các văn bản khoa học, chính trị) và phần lớn các bức ảnh/văn bản khác chưa được gán nhãn được thu thập từ internet. Thực tế cho thấy rất nhiều các bài toán Machine Learning thuộc vào nhóm này vì việc thu thập dữ liệu có nhãn tốn rất nhiều thời gian và có chi phí cao. Rất nhiều loại dữ liệu thậm chí cần phải có chuyên gia mới gán nhãn được (ảnh y học chẳng hạn). Ngược lại, dữ liệu chưa có nhãn có thể được thu thập với chi phí thấp từ internet.

### 4. **Reinforcement Learning (Học tăng cường)**

Reinforcement learning là các bài toán giúp cho một hệ thống tự động xác định hành vi dựa trên hoàn cảnh để đạt được lợi ích cao nhất (maximizing the performance). Hiện tại, Reinforcement learning chủ yếu được áp dụng vào Lý Thuyết Trò Chơi (Game Theory), các thuật toán cần xác định nước đi tiếp theo để đạt được điểm số cao nhất.

![image](https://user-images.githubusercontent.com/87793139/149309650-d0744a7d-1f47-4505-90f5-5552ac9ad58f.png)

*Ví dụ:* AlphaGo gần đây nổi tiếng với việc chơi cờ vây thắng cả con người. Cờ vây được xem là có độ phức tạp cực kỳ cao với tổng số nước đi là xấp xỉ 10^761, so với cờ vua là 10^120 và tổng số nguyên tử trong toàn vũ trụ là khoảng 10^80!! Vì vậy, thuật toán phải chọn ra 1 nước đi tối ưu trong số hàng nhiều tỉ tỉ lựa chọn. Về cơ bản, AlphaGo bao gồm các thuật toán thuộc cả Supervised learning và Reinforcement learning. Trong phần Supervised learning, dữ liệu từ các ván cờ do con người chơi với nhau được đưa vào để huấn luyện. Tuy nhiên, mục đích cuối cùng của AlphaGo không phải là chơi như con người mà phải thậm chí thắng cả con người. Vì vậy, sau khi học xong các ván cờ của con người, AlphaGo tự chơi với chính nó với hàng triệu ván chơi để tìm ra các nước đi mới tối ưu hơn. Thuật toán trong phần tự chơi này được xếp vào loại Reinforcement learning.

## **II. Các thuật toán Machine Learning thường được sử dụng**

Dưới đây là danh sách các thuật toán học máy thường được sử dụng. Các thuật toán này có thể được áp dụng cho hầu hết mọi vấn đề về dữ liệu:

1. Linear Regression
1. Logistic Regression
1. Decision Tree
1. SVM
1. Naive Bayes
1. KNN
1. K-Means
1. Random Forest
1. Dimensionality Reduction Algorithms
1. Gradient Boosting algorithms

### **1. Linear Regression**

Được sử dụng để ước tính giá trị thực (chi phí nhà, số lượng cuộc gọi, tổng doanh số bán hàng, v.v.) dựa trên (các) biến liên tục. Ở đây, chúng ta thiết lập mối quan hệ giữa các biến độc lập và phụ thuộc bằng cách đặt một đường thẳng tốt nhất. Đường phù hợp nhất này được gọi là đường hồi quy và được biểu diễn bằng phương trình tuyến tính Y = a \* X + b.

Trong phương trình này:

Y - Biến phụ thuộc

a - độ dốc

X - Biến độc lập

b - hệ số chặn

Các hệ số a và b này được suy ra dựa trên việc giảm thiểu tổng bình phương chênh lệch khoảng cách giữa các điểm dữ liệu và đường hồi quy.

Nhìn vào ví dụ dưới đây. Ở đây chúng ta xác định được đường phù hợp nhất có phương trình tuyến tính y = 0,2811x + 13,9. Bây giờ sử dụng phương trình này, chúng ta có thể tìm cân nặng, biết chiều cao của một người.

![image](https://user-images.githubusercontent.com/87793139/149309699-fcdc7e49-d899-4d55-92fe-617df99bae8e.png)

Hồi quy tuyến tính chủ yếu có hai loại: Hồi quy tuyến tính đơn và hồi quy tuyến tính bội. Hồi quy tuyến tính đơn được đặc trưng bởi một biến độc lập. Và hồi quy tuyến tính bội được đặc trưng bởi nhiều hơn 1 biến độc lập.

## **2. Logistic Regression**

Được sử dụng để ước tính các giá trị rời rạc (Giá trị nhị phân như 0/1, yes/no, true/false) dựa trên tập hợp (các) biến độc lập đã cho. Nói một cách đơn giản, nó dự đoán xác suất xảy ra một sự kiện bằng cách khớp dữ liệu với một hàm logit. Do đó, nó còn được gọi là hồi quy logit. Vì nó dự đoán xác suất, các giá trị đầu ra của nó nằm trong khoảng từ 0 đến 1.

![image](https://user-images.githubusercontent.com/87793139/149309744-569224ad-ff24-46dd-8cf6-1d50c71d3695.png)

## **3. Decision Tree**

Cây quyết định (Decision Tree) là một cây phân cấp có cấu trúc được dùng để phân lớp các đối tượng dựa vào dãy các luật. Các thuộc tính của đối tượng có thể thuộc các kiểu dữ liệu khác nhau như Nhị phân (Binary) , Định danh (Nominal), Thứ tự (Ordinal), Số lượng (Quantitative) trong khi đó thuộc tính phân lớp phải có kiểu dữ liệu là Binary hoặc Ordinal.

Xét một ví dụ 1 kinh điển khác về cây quyết định. Giả sử dựa theo thời tiết mà các bạn sẽ quyết định đi chơi hay không?

Những đặc điểm ban đầu là: thời tiết, độ ẩm, gió.

Dựa vào những thông tin trên, ta có thể xây dựng được mô hình như sau:

![image](https://user-images.githubusercontent.com/87793139/149309771-686bcac4-0dfa-4231-b4f6-394e90817e11.png)

## **4. SVM (Support Vector Machine)**

SVM (Support Vector Machine) là một thuật toán học máy có giám sát, sử dụng kỹ thuật ánh xạ dữ liệu vào một không gian nhiều chiều hơn để thuận tiện cho việc tìm ra ranh giới phân chia dữ liệu.

Mục tiêu của SVM là tìm ra một siêu phẳng trong không gian N chiều (ứng với N đặc trưng) chia dữ liệu thành hai phần tương ứng với lớp của chúng. Nói theo ngôn ngữ của đại số tuyển tính, siêu phẳng này phải có lề cực đại và phân chia hai bao lồi và cách đều chúng.

![image](https://user-images.githubusercontent.com/87793139/149309794-7d207664-6334-4ff4-9c37-fd422d9f587c.png)

Một điểm trong không gian véc tơ có thể được coi là một véc tơ từ gốc tọa độ tới điểm đó. Các điểm dữ liệu nằm trên hoặc gần nhất với siêu phẳng được gọi là véc tơ hỗ trợ, chúng ảnh hưởng đến vị trí và hướng của siêu phẳng. Các véc tơ này được sử dụng để tối ưu hóa lề và nếu xóa các điểm này, vị trí của siêu phẳng sẽ thay đổi. Một điểm lưu ý nữa đó là các véc tơ hỗ trợ phải cách đều siêu phẳng.

![image](https://user-images.githubusercontent.com/87793139/149309829-e74ea010-55b4-4727-a570-cc889ed8581b.png)

## **5. Naive Bayes**

Công thức Bayes:

![image](https://user-images.githubusercontent.com/87793139/149309850-26a69cd5-629f-4539-a610-c8de652c890f.png)

P(A|B) là “xác suất của A khi biết B”.

P(A) là xác suất xảy ra của A.

P(B|A) là “xác suất của B khi biết A”.

P(B) là xác suất xảy ra của B.

Naive Bayes là một thuật toán phân loại cho các vấn đề phân loại nhị phân (hai lớp) và đa lớp. Thuật toán Naive Bayes tính xác suất cho các yếu tố, sau đó chọn kết quả với xác suất cao nhất.

Tuy nhiên, ta cần lưu ý giả định của thuật toán Naive Bayes là các yếu tố đầu vào được cho là độc lập với nhau.

Thuật toán này là một thuật toán mạnh mẽ trong các bài toán dự đoán với thời gian thực; phân loại, lọc thư rác; hệ thống Recommendation.

*Ví dụ:* Dưới đây ta có một bộ dữ liệu đào tạo về thời tiết và biến mục tiêu “Play”. Bây giờ, chúng ta cần phân loại xem người chơi có chơi hay không dựa trên điều kiện thời tiết.

*Bước 1:* Chuyển đổi bộ dữ liệu thành bảng tần số.

*Bước 2:* Tạo bảng Khả năng xảy ra bằng cách tìm các xác suất như xác suất Overcast = 0.29 và xác suất đi chơi là 0.64.

![image](https://user-images.githubusercontent.com/87793139/149309874-70ef5a69-8993-4572-896a-e6f414d525ea.png)

*Bước 3:* Sử dụng Naive Bayes để tính xác suất sau cho từng lớp. Lớp có xác suất cao nhất là kết quả của dự đoán.

Giả sử xét câu nói: Bạn sẽ đi chơi nếu trời nắng. Câu nói này có đúng không?

Áp dụng Bayes: P(Yes | Sunny) = P(Sunny | Yes) \* P(Yes) / P (Sunny)

Ta có: P (Sunny | Yes) = 3/9 = 0.33, P(Sunny) = 5/14 = 0.36, P(Yes)= 9/14 = 0.64.

Vậy P(Yes | Sunny) = 0.33 \* 0.64 / 0.36 = 0.6.

Naive Bayes sử dụng một phương pháp tương tự để dự đoán xác suất của các lớp khác nhau dựa trên các thuộc tính khác nhau. Thuật toán này chủ yếu được sử dụng trong phân loại văn bản và gặp sự cố khi có nhiều lớp.

## **6. KNN (K-Nearest Neighbors)**

KNN là một trong những thuật toán supervised-learning đơn giản nhất mà hiệu quả trong một vài trường hợp trong Machine Learning. Khi training, thuật toán này không học một điều gì từ dữ liệu training (đây cũng là lý do thuật toán này được xếp vào loại lazy learning), mọi tính toán được thực hiện khi nó cần dự đoán kết quả của dữ liệu mới. Lớp (nhãn) của một đối tượng dữ liệu mới có thể dự đoán từ các lớp (nhãn) của k hàng xóm gần nó nhất.

*Ví dụ:* Bạn có điểm của một môn học nhưng bạn không biết thuộc loại nào (Giỏi, khá, trung bình, yếu). Giả sử bạn không biết bất kì quy tắc nào để phân loại cả. Có một cách giải quyết là bạn phải đi khảo sát những người xung quanh. Để biết điểm của mình thuộc loại nào thì bạn phải đi hỏi những đứa có điểm gần số điểm mình nhất. Giả sử trong lớp 50 đứa, mình khảo sát 5 đứa gần điểm mình nhất và được dữ liệu như sau:

Điểm của tôi: 7

Điểm của bạn tôi:

7.1 => Khá

7.2 => Khá

6.7 => Khá

6.6 => Khá

6.4 => Trung bình

Qua kết quả trên thì mình sẽ mạnh dạng đoán là mình loại khá. Với cách này chúng ta có thể phân loại dữ liệu 1 chiều (1 feature) bằng cách làm khá đơn giản. Và ta nhận thấy rằng dữ liệu mình khảo sát càng nhiều, càng rộng thì dự đoán đưa ra càng chính xác (nhưng giả sử lớp bạn không có ai loại khá ngoài bạn thì cho dù bạn lấy bao nhiêu người gần điểm bạn nhất củng sẽ ra kết quả sai).

**\* Các bước trong KNN**

*Bước 1:* Ta có D là tập các điểm dữ liệu đã được gắn nhãn và A là dữ liệu chưa được phân loại.

*Bước 2:* Đo khoảng cách (Euclidian, Manhattan, Minkowski, Minkowski hoặc Trọng số) từ dữ liệu mới A đến tất cả các dữ liệu khác đã được phân loại trong D.

*Bước 3:* Chọn K (K là tham số tự định nghĩa) khoảng cách nhỏ nhất.

*Bước 4:* Kiểm tra danh sách các lớp có khoảng cách ngắn nhất và đếm số lượng của mỗi lớp xuất hiện.

*Bước 5:* Lớp của dữ liệu mới là lớp xuất hiện nhiều lần nhất.

## **7. K-Means**

K-means là một thuật toán phân cụm đơn giản thuộc loại học không giám sát (tức là dữ liệu không có nhãn) và được sử dụng để giải quyết bài toán phân cụm. Ý tưởng của thuật toán phân cụm k-means là phân chia một bộ dữ liệu thành các cụm khác nhau. Trong đó số lượng cụm được cho trước là k. Công việc phân cụm được xác lập dựa trên nguyên lý: Các điểm dữ liệu trong cùng một cụm thì phải có cùng một số tính chất nhất định. Tức là giữa các điểm trong cùng một cụm phải có sự liên quan lẫn nhau. Đối với máy tính thì các điểm trong một cụm đó sẽ là các điểm dữ liệu gần nhau.

Thuật toán phân cụm k-means thường được sử dụng trong các ứng dụng cỗ máy tìm kiếm, phân đoạn khách hàng, thống kê dữ liệu,…

**\* Các bước của giải thuật K-Means**

Thuật toán K-Means lặp đi lặp lại quá trình phân các ví dụ vào cụm có tâm gần nhất, sau đó là điều chỉnh tâm cụm, cho tới khi điều kiện hội tụ được thỏa mãn. Cụ thể hơn, thuật toán được biểu diễn qua các bước sau:

*Bước 1:* Khởi tạo ngẫu nhiên tâm cụm: chọn ngẫu nhiên k ví dụ trong tập data làm k cụm khởi đầu.

*Bước 2:* Gán từng ví dụ vào cụm có tâm gần nó nhất. Việc tính khoảng cách từ một điểm tới một tâm cụm có thể tính dựa theo khoảng cách hình học Euclid.

*Bước 3:* Điều chỉnh tâm cụm: tọa độ của tâm cụm mới bằng tọa độ trung bình của tất cả các ví dụ trong cụm đó.

*Bước 4:* Kiểm tra điều kiện dừng: nếu thuật toán chưa hội tụ, quay lại bước 2.

Lưu ý: Điều kiện dừng có thể được định nghĩa bằng số vòng lặp giới hạn, hoặc khi không có sự thay đổi về vị trí của tâm cụm.

*Ví dụ:* Ban đầu, ta có một tập dữ liệu chưa được phân cụm như thế này.

![image](https://user-images.githubusercontent.com/87793139/149309910-1868ff25-211d-45b7-9264-ba14e9ed4b6a.png)

Chọn ngẫu nhiên 3 tâm cụm khởi đầu.

![image](https://user-images.githubusercontent.com/87793139/149309936-e540d43b-485d-4e03-b361-9ac97d294c31.png)

Gán các ví dụ vào cụm có tâm gần nó nhất.

![image](https://user-images.githubusercontent.com/87793139/149309962-304ec8e4-8680-4271-844a-570e9a562467.png)

Điều kiện hội tụ chưa thỏa mãn, thực hiện lại việc gán các ví dụ vào cụm có tâm gần nó nhất.

![image](https://user-images.githubusercontent.com/87793139/149309975-7e7e40dc-e865-422d-b347-2285cc429539.png)

Điều chỉnh tâm cụm.

![image](https://user-images.githubusercontent.com/87793139/149310000-fd8e740a-b9f6-493e-b4e6-46c0148045c2.png)

Điều kiện hội tụ chưa thỏa mãn, thực hiện lại việc gán các ví dụ vào cụm có tâm gần nó nhất.

![image](https://user-images.githubusercontent.com/87793139/149310021-7b168b61-5253-4c8a-80d9-3ef9d3d5f378.png)

Điều chỉnh tâm cụm.

![image](https://user-images.githubusercontent.com/87793139/149310037-5b336e2d-dc2c-4bcf-b902-0a48e6593fde.png)

## **8. Random Forest**

Random Forest là thuật toán học có giám sát (supervised learning). Nó có thể được sử dụng cho cả phân lớp và hồi quy. Nó cũng là một trong những thuật toán linh hoạt và dễ sử dụng nhất. Random forest tạo ra cây quyết định trên các mẫu dữ liệu được chọn ngẫu nhiên, được dự đoán từ mỗi cây và chọn giải pháp tốt nhất bằng cách bỏ phiếu. Như tên gọi của nó, Rừng ngẫu nhiên sử dụng các cây (tree) để làm nền tảng. Rừng ngẫu nhiên là một tập hợp của các Decision Tree, mà mỗi cây được chọn theo một thuật toán dựa vào ngẫu nhiên.

*Ví dụ:* Giả sử bạn muốn đi trên một chuyến đi và bạn muốn đi đến một nơi mà bạn sẽ thích. Bạn quyết định hỏi bạn bè và nói chuyện với họ về trải nghiệm du lịch trong quá khứ của họ đến những nơi khác nhau. Bạn sẽ nhận được một số khuyến nghị từ tất cả các bạn. Bây giờ bạn phải tạo danh sách các địa điểm được đề xuất. Sau đó, bạn nhờ họ bỏ phiếu (hoặc chọn địa điểm tốt nhất cho chuyến đi) từ danh sách các địa điểm được đề xuất bạn đã thực hiện. Địa điểm có số phiếu bầu cao nhất sẽ là lựa chọn cuối cùng của bạn cho chuyến đi.

**\* Các bước hoạt động của thuật toán:**

*Bước 1:* Chọn các mẫu ngẫu nhiên từ tập dữ liệu đã cho.

*Bước 2:* Thiết lập cây quyết định cho từng mẫu và nhận kết quả dự đoán từ mỗi quyết định cây.

*Bước 3:* Bỏ phiếu cho mỗi kết quả dự đoán.

*Bước 4:* Chọn kết quả được dự đoán nhiều nhất là dự đoán cuối cùng.

![image](https://user-images.githubusercontent.com/87793139/149310058-374f03e8-a9b1-439d-aef8-d49a8ef58661.png)

## **9. Dimensionality Reduction Algorithms**

Với kỷ nguyên dữ liệu như hiện nay, một tập dữ liệu high-dimension (đa chiều) với hàng nghìn feature hay cột đã trở thành điều không quá xa lạ. High-dimension data mở hướng cho nhiều cách xử lý các bài toán phức tạp trong thực tế, có thể kể đến dự đoán cấu trúc protein liên quan COVID-19, phân tích hình ảnh MEG scan não, v.v. Tuy nhiên, một tập dữ liệu high-dimension lại thường chứa các feature kém (không đóng góp nhiều vào kết quả) dẫn đến việc giảm hiệu năng của mô hình. Và việc lựa chọn trong rất nhiều feature để chọn ra feature có ảnh hưởng lớn đến kết quả cũng trở nên khó khăn hơn.

Một phương pháp thường được áp dụng là kỹ thuật dimensional reduction (hay giảm chiều dữ liệu). Ưu điểm của phương pháp này bao gồm:

\+ Cải thiện độ chính xác của model do giảm thiểu điểm dữ liệu dư thừa, nhiễu.

\+ Model huấn luyện nhanh hơn (do dimension đã giảm) và giảm tài nguyên sử dụng để tính toán.

\+ Kết quả của mô hình có thể được phân tích dễ dàng hơn.

\+ Giảm overfitting trong nhiều trường hợp. Với quá nhiều feature trong dữ liệu, mô hình trở nên phức tạp và có xu hướng overfit trên tập huấn luyện.

\+ Dễ dàng hơn trong việc visualize dữ liệu (plot trên miền 2D hay 3D).

\+ Giảm thiểu trường hợp multicolinearity (đa cộng tuyến tính). Trong các bài toán regression, multicolinearity xảy ra khi các biến độc lập trong mô hình phụ thuộc tuyến tính lẫn nhau.

*Các phương pháp thường chia thành hai hướng:*

\+ Feature Selection: Lựa chọn và giữ lại các feature tốt.

\+ Feature Extraction: Giảm chiều dữ liệu bằng các kết hợp các feature đang có.

![image](https://user-images.githubusercontent.com/87793139/149310090-cb600b7a-655a-4782-8231-2bfbb1abd102.png)

## **10. Gradient Boosting Algorithms**

Boosting là một kĩ thuật đồng bộ nhằm cố gắng tạo ra một phương pháp phân loại mạnh từ một số phương pháp phân loại yếu. Điều này được thực hiện bằng cách xây dựng mô hình từ dữ liệu đào tạo, sau đó tạo ra một mô hình thứ hai cố gắng sửa lỗi từ mô hình đầu tiên. Các mô hình được thêm vào cho đến khi tập đào tạo được dự đoán hoàn hảo hoặc thêm một số mô hình tối đa.

AdaBoost, tên đầy đủ là Adaptive Boosting, là thuật toán thuộc nhánh Boosting trong Ensemble learning. Với ý tưởng đơn giản là sử dụng các cây quyết định (1 gốc, 2 lá) để đánh trọng số cho các điểm dữ liệu, từ đó tối thiểu hóa trọng số các điểm bị phân loại sai (trọng số lớn), để tăng hiệu suất của mô hình.

![image](https://user-images.githubusercontent.com/87793139/149310119-2ff186dd-2cd4-416c-b8b7-1da9d4cb80e8.png)
