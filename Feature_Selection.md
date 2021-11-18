# Tại sao cần trích chọn đặc trưng?
Trong xây dựng mô hình máy học, lượng đặc trưng quá nhiều sẽ khiến cho quá trình huấn luyện, quá trình phân loại mất nhiều thời gian hơn. Chính vì thế, ta cần một giải pháp để giải quyết vấn đề này.

Trích chọn đặc trưng (feature selection hay còn gọi với các tên khác như là variable selection, attribute selection hay variable subset selection) là một quá trình chọn lọc một tập con chứa các đặc trưng liên quan, loại bỏ những dữ liệu dư thừa mà vẫn đảm bảo độ chính xác, nâng cao hiệu quả dự đoán cho các mô hình máy học. Việc trích chọn đặc trưng giải quyết được vấn đề đã đặt ra.

# Các phương pháp trích chọn đặc trưng
Có 3 phương pháp để trích chọn đặc trưng, chúng được phân chia dựa trên sự tương tác với mô hình học máy như phương pháp Filter, Wrapper và Embedded. 

Từng phương pháp học máy sẽ có những phương pháp tương ứng hiệu quả riêng với nó. Hiểu ngắn gọn, không có phương pháp vạn năng nào. 

## Filter Methods
Trong Filter, các đặc tính được chọn dựa trên các phương pháp thống kê dựa trên chấm điểm tiêu chí liên quan. Nó độc lập với thuật toán học và cần ít thời gian tính toán hơn. Nó chủ yếu được biết đến như một phương pháp nhanh và tổng quát, nhưng có xu hướng chọn các tập con đầu ra lớn.

Một số các phương thức đo lường thống kê được sử dụng trong Filter bao gồm Information gain, Chi-square test, Fisher's score, correlation coef-ficient, và variance threshold. 

### 1. Variance Threshold
Variance Threshold (tạm dịch là Ngưỡng phương sai) là một cách tiếp cận đơn giản với trích chọn đặc trưng. Nó loại bỏ tất cả các tính năng mà phương sai không đáp ứng đủ ngưỡng. Các đặc trưng có phương sai cao hơn có thể chứa nhiều thông tin hữu ích hơn.
Phương pháp này không tính đến mối quan hệ giữa các đặc trưng hoặc giữa các đặc trưng và mục tiêu, chính vì thế, đây là một trong những hạn chế của phương pháp lọc (Filter)

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2020/10/Image-6-1.png)

Hàm get_support() trả về một vectơ Boolean trong đó True có nghĩa là biến không có phương sai bằng không.

### 2. Fisher's Score
Fisher's Score là một trong những phương pháp trích chọn đặc trưng được sử dụng phổ biến nhất. Thuật toán này sẽ trả về thứ hạng của các biến dựa trên Fisher's Score theo thứ tự giảm dần. Chúng ta có thể chọn các biến tùy theo trường hợp mong muốn.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2020/10/Image-4-1.png)

### 3. Correlation Coefficient
Tương quan là thước đo mối quan hệ tuyến tính của 2 hoặc nhiều biến đặc trưng. 

Thông qua mối tương quan, nếu hai biến có tương quan, chúng ta có thể dự đoán biến này từ biến khác. Do đó, nếu hai đặc trưng có tương quan với nhau, thì mô hình chỉ thực sự cần một trong số chúng, vì đặc trưng thứ hai không bổ sung thêm thông tin. Ta sẽ sử dụng Tương quan Pearson ở đây.

Ngoài ra, đặc trưng tốt hơn có tương quan với mục tiêu cao hơn. Vậy, các biến đặc trưng được chọn sẽ có tương quan với biến mục tiêu hơn và không nên tương quan với nhau.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2020/10/Image-5-1.png)

Chúng ta cần đặt một giá trị tuyệt đối, chẳng hạn như 0,5 làm ngưỡng để chọn các biến.
Nếu nhận thấy các biến dự báo rằng giữa 2 hay nhiều đặc trưng có tương quan với nhau, chúng ta có thể loại bỏ biến có giá trị hệ số tương quan thấp hơn với biến mục tiêu.
Chúng ta cũng có thể tính toán nhiều hệ số tương quan để kiểm tra xem có hơn hai biến có tương quan với nhau hay không. Hiện tượng này được gọi là đa cộng tuyến.

### 4. Chi-square Test

Chi-square Test được sử dụng trong việc phân loại đặc trưng trong tập dữ liệu.
Ta sẽ tiến hành tính toán Chi-square giữa mỗi đặc trưng và mục tiêu rồi chọn ra số lượng đặc trưng mong muốn có điểm Chi-square tốt nhất.
Để áp dụng chính xác phương pháp Chi-Square Test nhằm kiểm tra mối quan hệ giữa mỗi tính năng khác nhau trong tập dữ liệu và biến mục tiêu, phải đáp ứng những điều kiện sau: các biến đặc trưng phải được phân loại, được lấy mẫu độc lập và các giá trị phải có tần suất mong đợi lớn hơn 5.

![](https://user-images.githubusercontent.com/84955172/142258540-a87bfb69-e593-42e4-94a8-150c6460aa17.png)


## Wrapper Methods
Khác với Filter, Wrapper sử dụng các kỹ thuật máy học để đánh giá tập con các đặc trưng theo tiêu chuẩn tương ứng. Hiệu suất của Wrapper phụ thuộc vào các thuật toán phân loại. Tập hợp con tốt nhất của các đặc trưng được chọn dựa trên kết quả của thuật toán phân loại.
Về mặt tính toán, các phương pháp Wrapper yêu cầu tính toán phức tạp hơn các Filter, do các bước học tập lặp lại và xác nhận chéo. Tuy nhiên, các phương pháp này chính xác hơn Filter.
Phương pháp này không được khuyến cáo với số lượng đặc trưng quá cao.

Một số thuật toán được sử dụng trong Wrapper là Recursive feature elimination, Forward Feature Selection, and Backward Feature Elimination, Bi-directional elimination.

### 1. Forward Feature Selection
Đây là một phương pháp lặp lại.
Khi bắt đầu, mảng đặc trưng được chọn chưa có đặc trưng nào. Sau đó, bắt đầu thêm vào đó từng đặc trưng đầu tiên với giá trị p nhỏ nhất trên tập đặc trưng.
Thêm đặc trưng thứ hai bằng cách thử kết hợp đặc trưng đã chọn trước đó với tất cả các đặc trưng còn lại khác. Một lần nữa chọn đặc trưng có giá trị p nhỏ nhất. 
Lặp lại quá trình này cho đến khi đạt được tiêu chí đặt trước, tức ta sẽ có một tập hợp các đặc trưng đã chọn với giá trị p của các đặc trưng riêng lẻ nhỏ hơn ngưỡng.

![](https://user-images.githubusercontent.com/84955172/142262936-e9391e40-ae41-423b-9c53-92603faaa8e0.png)

### 2. Backward Feature Elimination
Phương thức này hoạt động hoàn toàn ngược lại với phương pháp Forward Feature Selection. Trong loại bỏ ngược, chúng ta bắt đầu với mảng đặc trưng đầy đủ (bao gồm tất cả các biến độc lập) và sau đó loại bỏ đặc trưng không quan trọng với giá trị p cao nhất (> mức ý nghĩa). 
Quá trình này lặp đi lặp lại nhiều lần cho đến khi ta có được tập hợp các tính năng quan trọng cuối cùng.
Phương pháp này cùng với phương pháp Forward Feature Selection còn được gọi là phương pháp Sequential Feature Selection.

![](https://user-images.githubusercontent.com/84955172/142373894-2d583e8f-3350-41c8-a8a5-856324124d40.png)

### 3. Bi-directional elimination
Nó tương tự như Forward Feature Selection nhưng sự khác biệt là trong khi thêm một tính năng mới, nó cũng kiểm tra tầm quan trọng của các đặc trưng đã được thêm vào và nếu nó tìm thấy đặc trưng nào đã chọn là không đáng kể thì nó cần loại bỏ tính năng cụ thể đó thông qua Backward Feature Elimination.

## Embedded Methods
Phương pháp Embedded kết hợp ưu điểm của cả hai phương pháp Wrapper và Filter. Nó có các ưu điểm bao gồm giúp cho thuật toán máy học huấn luyện nhanh hơn so với phương pháp Wrapper, giảm độ phức tạp của mô hình và làm cho mô hình dễ biên dịch, chính xác hơn so với phương pháp Filter.

Một số thuật toán được sử dụng trong Embedded là Lasso Regression, Ridge Regression, Random Forest Importance.

### 1. LASSO Regularization (L1)

### 2. Random Forest Importance
Random Forests là một loại Bagging Algorithm. Phương pháp này cho phép nhiều cây đặc trưng 
Random Forests is a kind of a Bagging Algorithm that aggregates a specified number of decision trees. 

## Tổng quan
Các phương pháp đều có điểm chung là chấm điểm các features theo một giá trị, hoặc một công thức nào đó. Từ đó, ta có thể chọn ra một số lượng feature nhất định thông qua ngưỡng giá trị điểm đã chấm. 


https://www.analyticsvidhya.com/blog/2020/10/a-comprehensive-guide-to-feature-selection-using-wrapper-methods-in-python/
https://www.analyticsvidhya.com/blog/2020/10/feature-selection-techniques-in-machine-learning/
