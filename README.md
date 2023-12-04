# spam_detect
1.	Biến data gán cho hàm đọc file csv.
2.	Các biến emails và lables để chứa dữ liệu từ các cột Message và Catgory tương ứng trong file csv.
3. 	Hàm train_test_split() dùng để chia dữ liệu thành tập huấn luyện và tập thử với kích thước thử là 20% và
    trạng thái ngẫu nhiên với số 42 (đặt trạng thái ngẫu nhiên thành một giá trị cố định, chẳng hạn như 42,
	  đảm bảo rằng việc phân tách thử nghiệm đào tạo sẽ nhất quán trên các lần chạy mã khác nhau, giúp kết quả có thể lặp lại được).

4.	Hàm `CountVectorizer` được khởi tạo để chuyển đổi dữ liệu văn bản email thành các vectơ đặc
  	trưng số bằng cách sử dụng phương pháp Bag-of-Words. Nó tách rời các chữ cái và đếm sự xuất
  	hiện của mỗi từ.
5.	Hàm fit_transform() được áp dụng cho tập huấn luyện (`X_train`) để học từ vựng và chuyển các
  	email đào tạo thành ma trận đếm từ.
6.	Hàm transform() được áp dụng cho bộ kiểm tra (`X_test`) để chuyển đổi các email kiểm tra thành
  	cùng một ma trận đếm từ dựa trên từ vựng đã học.
7.	Hàm accuracy_score tính toán độ chính xác của mô hình bằng cách so sánh các nhãn được dự đoán
  	predictions với nhãn (`y_test`).

8.  Hàm precision_score tính toán độ chính xác của thuật toán cho lớp "spam".
10.	Hàm recall_score tính toán tỷ lệ true positive(TP) với tổng true postive(TP) và false negative (FN) 
11.	Hàm f1_score tính toán f1 (Là số dung hòa Recall và Precision) cho lớp "spam".
