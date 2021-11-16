# Trích chọn đặc trưng (Feature Selection)

## Tại sao cần trích chọn đặc trưng?
Trong xây dựng mô hình máy học, lượng đặc trưng quá nhiều sẽ khiến cho quá trình huấn luyện, quá trình phân loại mất nhiều thời gian hơn. Chính vì thế, ta cần một giải pháp để giải quyết vấn đề này.

Trích chọn đặc trưng (feature selection hay còn gọi với các tên khác như là variable selection, attribute selection hay variable subset selection) là một quá trình chọn lọc một tập con chứa các thuộc tính liên quan, loại bỏ những dữ liệu dư thừa mà vẫn đảm bảo độ chính xác, nâng cao hiệu quả dự đoán cho các mô hình máy học. Việc trích chọn đặc trưng giải quyết được vấn đề đã đặt ra.

## Các phương pháp trích chọn đặc trưng
Có 3 phương pháp để trích chọn đặc trưng, chúng được phân chia dựa trên sự tương tác với mô hình học máy như phương pháp Filter, Wrapper và Embedded. 

Từng phương pháp học máy sẽ có những phương pháp tương ứng hiệu quả riêng với nó. Hiểu ngắn gọn, không có phương pháp vạn năng nào. 

### Filter
Trong Filter, các đặc tính được chọn dựa trên các phương pháp thống kê dựa trên chấm điểm tiêu chí liên quan. Nó độc lập với thuật toán học và cần ít thời gian tính toán hơn. Nó chủ yếu được biết đến như một phương pháp nhanh và tổng quát, nhưng có xu hướng chọn các tập con đầu ra lớn.

Một số các phương thức đo lường thống kê được sử dụng trong Filter bao gồm Information gain, Chi-square test, Fisher score, correlation coef-ficient, và variance threshold. 
### Wrapper
Khác với Filter, Wrapper sử dụng các kỹ thuật máy học để đánh giá tập con các thuộc tính theo tiêu chuẩn tương ứng. Hiệu suất của Wrapper phụ thuộc vào các thuật toán phân loại. Tập hợp con tốt nhất của các đặc tính được chọn dựa trên kết quả của thuật toán phân loại.
Về mặt tính toán, các phương pháp Wrapper yêu cầu tính toán phức tạp hơn các Filter, do các bước học tập lặp lại và xác nhận chéo. Tuy nhiên, các phương pháp này chính xác hơn Filter.
Phương pháp này không được khuyến cáo với số lượng đặc tính quá cao.

Một số thuật toán được sử dụng trong Wrapper là Recursive feature elimination, Sequential feature selection algorithms, and Genetic algorithms. 
### Embedded
Cách tiếp cận thứ ba là phương pháp Embedded sử dụng phương pháp học tập kết hợp và phương pháp lai để lựa chọn đặc tính, giải pháp trích chọn đặc trưng này ra đời để giải quyết bài toán trên. Nó có các ưu điểm bao gồm giúp cho thuật toán máy học huấn luyện nhanh hơn so với phương pháp Wrapper, giảm độ phức tạp của mô hình và làm cho mô hình dễ biên dịch, chính xác hơn so với phương pháp Filter.

Một số thuật toán được sử dụng trong Embedded là Lasso Regression, Ridge Regression, Tree importance.
### Tổng quan
Các phương pháp đều có điểm chung là chấm điểm các features theo một giá trị, hoặc một công thức nào đó. Từ đó, ta có thể chọn ra một số lượng feature nhất định thông qua ngưỡng giá trị điểm đã chấm. 


## Quy trình trích chọn đặc trưng
