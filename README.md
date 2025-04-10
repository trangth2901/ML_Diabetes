# ML_Diabetes
## Giới thiệu
Bệnh đái tháo đường (tiểu đường) là một rối loạn chuyển hóa đặc trưng bởi tình trạng lượng đường huyết tăng cao bất thường, thường do sự mất cân bằng insulin trong cơ thể. Bệnh nếu không được kiểm soát tốt có thể gây ra các biến chứng nghiêm trọng như đột quỵ, suy thận, và bệnh tim mạch.

Nghiên cứu này nhằm dự đoán khả năng mắc bệnh tiểu đường của bệnh nhân dựa trên các đặc trưng y tế thu thập được. Việc phát hiện sớm và chính xác sẽ giúp người bệnh chủ động điều trị, kiểm soát đường huyết, giảm thiểu rủi ro và nâng cao chất lượng cuộc sống.

## Mục tiêu đề tài
* Dự đoán khả năng mắc bệnh tiểu đường dựa trên các thông số y tế cơ bản của bệnh nhân.
* Ứng dụng các kỹ thuật học máy để xây dựng mô hình phân loại có độ chính xác cao.
* Hỗ trợ việc phát hiện sớm bệnh tiểu đường, từ đó giúp người bệnh chủ động trong việc phòng ngừa và điều trị.

## Thành viên nhóm 
* A46350 Trần Huyền Trang
* A42661 Phạm Văn Tài

## Công nghệ sử dụng
* Ngôn ngữ lập trình: Python
* Thư viện chính: Pandas, Scikit-learning, Seaborn, Matplotlib
* Mô hình: Decision Tree, Logistic Regression, SVM

## Bộ dữ liệu sử dụng
Bộ dữ liệu Pima Indians Diabetes Database là một tập dữ liệu nổi tiếng trong lĩnh vực y tế và học máy, được cung cấp bởi Viện Quốc gia về Bệnh tiểu đường, Tiêu hóa và Thận của Hoa Kỳ (NIDDK). Mục tiêu của bộ dữ liệu là dự đoán liệu một bệnh nhân có mắc bệnh tiểu đường hay không dựa trên các chỉ số y tế đo được từ các phụ nữ người Mỹ bản địa Pima, từ 21 tuổi trở lên.

(https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

## Kết quả và Đánh giá

| Mô hình                | Accuracy | Precision | Recall  | F1-Score | AUC-ROC | 
|------------------------|----------|-----------|---------|----------|---------|
| Logistic Regression    | 0.7800   | 0.7673    | 0.8079  | 0.7871   | 0.8503  | 
| SVM                    | 0.7667   | 0.7647    | 0.7748  | 0.7697   | 0.8369  | 
| Decision Tree          | 0.7700   | 0.7228    | 0.8808  | 0.7940   | 0.8029  | 

* Nhìn chung tất cả các mô hình
đã đạt được mục tiêu chúng tôi đề ra (recall >0.7 và
AUC-ROC > 0.8)..
* Logistic Regression có tổng thể hiệu suất tốt nhất, với độ chính xác, Precision, Recall, F1-Score và AUC-ROC cao nhất. Đây là mô hình khá cân bằng giữa Precision và Recall.
* SVM có hiệu suất thấp hơn một chút so với Logistic Regression, đặc biệt ở các chỉ số Precision,
Recall và AUC-ROC. Decision Tree có Recall rất cao
(80.8%), nhưng Precision thấp và AUC-ROC thấp, cho thấy
mô hình này dễ bỏ sót các bệnh nhân mắc bệnh nhưng lại
đưa ra nhiều dự đoán sai về những người không mắc bệnh
