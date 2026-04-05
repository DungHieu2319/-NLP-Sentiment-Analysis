# 📊 Sentiment Analysis - Amazon Food Reviews

---

## 📌 Giới thiệu

Project này thực hiện **phân tích cảm xúc (Sentiment Analysis)** trên tập dữ liệu **Amazon Fine Food Reviews** bằng các mô hình Machine Learning và Deep Learning.

Mục tiêu của project là **phân loại các review của khách hàng thành Positive (tích cực) hoặc Negative (tiêu cực)** dựa trên nội dung văn bản của review.

---

## 📂 Dataset

Dataset sử dụng: **Amazon Fine Food Reviews** (https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews)

Dataset chứa các review sản phẩm thực phẩm trên Amazon trong hơn **10 năm**, bao gồm thông tin sản phẩm, người dùng, điểm đánh giá và nội dung review.

Các cột chính được sử dụng:
| Cột | Mô tả |
|----|------|
| Text | Nội dung review của khách hàng |
| Score | Số sao khách hàng đánh giá (1–5) |

---

## ⚙️ Data Preprocessing

Các bước tiền xử lý dữ liệu:

- Xóa **review trùng lặp**
- Xóa **giá trị null**
- Chuyển **rating thành sentiment label**
- Chuyển text về **lowercase**
- Loại bỏ **dấu câu**
- **Tokenization**
- **Stopword removal**
- Biểu diễn văn bản bằng **TF-IDF**

---

## 🤖 Các mô hình được sử dụng

Project sử dụng **5 mô hình để so sánh hiệu quả**:

| Model | Loại |
|------|------|
| Logistic Regression | Machine Learning |
| Naive Bayes | Machine Learning |
| Support Vector Machine (SVM) | Machine Learning |
| BiLSTM | Deep Learning |
| DistilBERT | Deep Learning (Transformer) |

---

## 📈 Kết quả mô hình

| Model | Accuracy | Nhận xét |
|------|---------|---------|
| Logistic Regression | ~0.88 | Kết quả tốt và ổn định |
| Naive Bayes | ~0.87 | Huấn luyện nhanh nhưng độ chính xác thấp hơn |
| SVM | ~0.89 | Hiệu quả tốt cho bài toán text classification |
| BiLSTM | ~0.87 | Không tối ưu cho dữ liệu text |
| **DistilBERT** | **~0.95** | **Mô hình tốt nhất** |

**DistilBERT đạt hiệu suất tốt nhất** do khả năng hiểu **ngữ cảnh và ý nghĩa của câu** tốt hơn các mô hình truyền thống.

---

## 🔎 Error Analysis

Một số trường hợp model dự đoán sai thường xảy ra khi:

- Review chứa **cả sentiment tích cực và tiêu cực**
- Có **sarcasm (mỉa mai)**
- Review **quá ngắn**
- Nội dung **không rõ cảm xúc**

---

## 💡 Ứng dụng thực tế

Sentiment Analysis có thể được ứng dụng trong nhiều lĩnh vực:

### E-commerce
- Phân tích review sản phẩm
- Đánh giá mức độ hài lòng của khách hàng

### Business Intelligence
- Theo dõi sentiment của khách hàng theo thời gian
- Phát hiện các vấn đề của sản phẩm

### Customer Support
- Tự động phát hiện **review tiêu cực**
- Ưu tiên xử lý complaint của khách hàng

### Social Media Analysis
- Phân tích ý kiến người dùng về **thương hiệu hoặc sản phẩm**

---

## 🛠 Công nghệ sử dụng

- Google Colab

---

# 📊 Workflow của Project

Dataset
↓
Data Cleaning
↓
Text Preprocessing
↓
Feature Engineering (TF-IDF)
↓
Train Models (5 models)
↓
Model Evaluation
↓
Error Analysis

---

## 📚 Kết luận

Project này so sánh hiệu quả của **các mô hình Machine Learning và Transformer** trong bài toán Sentiment Analysis.

Kết quả cho thấy **DistilBERT đạt hiệu suất tốt nhất**, chứng minh rằng **transformer-based models rất hiệu quả trong các bài toán NLP hiện đại**.