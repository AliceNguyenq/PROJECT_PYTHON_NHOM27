# PROJECT_PYTHON_NHOM27


<div align="center">
   
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)


</div>

## Description
Đây là dự án phân tích dữ liệu và xây dựng mô hình Machine Learning (Multi-class Classification) nhằm dự đoán gói cước 4G Viettel phù hợp cho từng khách hàng quốc tế đến Việt Nam.
Mục tiêu của dự án là:
- Phân tích dữ liệu khách hàng và dữ liệu hành trình của du khách quốc tế đến Việt Nam.
- Xây dựng mô hình Multi-class Classification dự đoán gói cước 4G Viettel phù hợp cho từng khách hàng.

## Dataset
Dự án gồm tập train và tập test đã chia sẵn, mỗi tập gồm 4 bảng dữ liệu chính:
1. train

| File                     | Nội dung                          | Kích thước      |
| ------------------------ | --------------------------------- | --------------- |
| **user.csv**             | Thông tin nhân khẩu học           | **11,572 × 16** |
| **context.csv**          | Thông tin chuyến đi               | **11,572 × 12** |
| **mobile_plan_user.csv** | Gói data được đề xuất & chấp nhận | **45,321 × 3**  |
| **mobile_plan_attr.csv** | Mô tả các gói data                | **5 × 4**       |


3. test

| File                     | Nội dung                          | Kích thước      |
| ------------------------ | --------------------------------- | --------------- |
| **user.csv**             | Thông tin nhân khẩu học           | **11,572 × 16** |
| **context.csv**          | Thông tin chuyến đi               | **11,572 × 12** |
| **mobile_plan_user.csv** | Gói data được đề xuất & chấp nhận | **45,321 × 3**  |
| **mobile_plan_attr.csv** | Mô tả các gói data                | **5 × 4**       |


## Cấu trúc project 
   project/
   │
   ├─ 📁 Result/                                      # Kết quả mô hình & log quá trình chạy
   │   ├── result_grid.csv                            # Kết quả GridSearchCV – bộ tham số tối ưu
   │   ├── result_random.csv                          # Kết quả RandomSearchCV
   │   ├── training.log                               # Log toàn bộ quá trình training (pipeline + model)
   │   └── (các file kết quả khác)
   │
   ├─ 📁 data train cleaned/                           # Dữ liệu TRAIN đã làm sạch & xử lý đặc trưng
   │   ├── user_train_cleaned.csv                     # User train sau khi xử lý missing/format
   │   ├── context_train_cleaned.csv                  # Context train đã chuẩn hóa time, location
   │   ├── mobile_plan_user_train_cleaned.csv         # Lịch sử gói cước đã clean (train)
   │   ├── mobile_plan_attr_train_cleaned.csv         # Mô tả gói cước đã chuẩn hóa (train)
   │   ├── merged_train_cleaned.csv                   # Bảng merged theo user_id – dataset hợp nhất
   │   ├── final_train_features.csv                   # Dataset cuối dùng để train mô hình
   │   └── (Tổng cộng: **6 file CSV**)
   │
   ├─ 📁 data test cleaned/                            # Dữ liệu TEST đã làm sạch & xử lý đặc trưng
   │   ├── user_test_cleaned.csv                      # User test sạch
   │   ├── context_test_cleaned.csv                   # Context test chuẩn hóa
   │   ├── mobile_plan_user_test_cleaned.csv          # Lịch sử gói test đã clean
   │   ├── mobile_plan_attr_test_cleaned.csv          # Mô tả gói test đã clean
   │   ├── merged_test_cleaned.csv                    # Dataset test hợp nhất
   │   ├── final_test_features.csv                    # Dataset đầu vào model khi predict
   │   └── (Tổng cộng: **6 file CSV**)
   │
   ├─ 📁 train data/                                   # Dữ liệu TRAIN thô (raw original data)
   │   ├── user.csv                                   # Thông tin nhân khẩu học ban đầu
   │   ├── context.csv                                # Thông tin chuyến đi ban đầu
   │   ├── mobile_plan_user.csv                       # Gói cước đề xuất/đã chọn (raw)
   │   ├── mobile_plan_attr.csv                       # Thông tin gói data (raw)
   │   └── (Tổng cộng: **4 file CSV**)
   │
   ├─ 📁 test data/                                    # Dữ liệu TEST thô (raw)
   │   ├── user_test.csv                              # User test nguyên bản
   │   ├── context_test.csv                           # Context test nguyên bản
   │   ├── mobile_plan_user_test.csv                  # Lịch sử gói test raw
   │   ├── mobile_plan_attr_test.csv                  # Mô tả gói test raw
   │   └── (Tổng cộng: **4 file CSV**)
   │
   ├─ 📁 notebooks/                                    # Notebook quy trình phân tích & mô hình
   │   ├── [NHOM27_PYTHON_1]_DataPreprocessing_NoneClass.ipynb   # Tiền xử lý dữ liệu không gộp (no aggregation)
   │   ├── [NHOM27_PYTHON_2]_DataPreprocessing_WithClass.ipynb   # Tiền xử lý dữ liệu có gộp (with aggregation)
   │   ├── [NHOM27_PYTHON_3]_EDA.ipynb                           # Phân tích dữ liệu khám phá (EDA)
   │   ├── [NHOM27_PYTHON_4]_Model_Final.ipynb                   # Xây dựng & đánh giá mô hình ML
   │
   │
   ├─ 📄 [NHOM27_PYTHON_5]_Report_File.pdf            # File báo cáo chính thức của nhóm
   ├─ 📄 LICENSE                                      # Giấy phép MIT License
   └─ 📄 README.md                                    # Tài liệu mô tả project



## Prerequisites
Before you begin, ensure you have met the following requirements:
- Python version >= 3.x
- Necessary libraries which can be found in `requirements.txt`
- Additional tools or resources needed to run this project

## Installation
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/AliceNguyenq/PROJECT_PYTHON_NHOM27.git
   ```
2. Navigate to the project directory:
   ```bash
   cd PROJECT_PYTHON_NHOM27
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Brief step-by-step guide to run the project:
   ```bash
   # Example command
   python main.py
   ```
2. Additional instructions on how to use the features of the project as needed.

## Contributing
To contribute to this project, follow these steps:
1. Fork this repository.
2. Create a branch: `git checkout -b feature-branch-name`.
3. Make your changes and commit them: `git commit -m 'Add new feature'`.
4. Push to the original branch: `git push origin feature-branch-name`.
5. Create the pull request.

Alternatively, see the GitHub documentation on [how to create a pull request](https://docs.github.com/articles/creating-a-pull-request).

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

### Acknowledgments
- Special thanks to Group 27 and contributors for their effort on this project.







# FINAL_PROJECT_DS_K23: HỆ THỐNG DỰ ĐOÁN GIÁ BẤT ĐỘNG SẢN

Dự án triển khai một **pipeline Học máy (Machine Learning Pipeline)** hoàn chỉnh theo kiến trúc **OOP (Lập trình hướng đối tượng)** để giải quyết bài toán **Hồi quy (Regression)** dự đoán giá căn hộ trên thị trường thứ cấp.

Pipeline bao gồm các module độc lập: Xử lý Dữ liệu Thô, Kỹ thuật Đặc trưng Chuyên biệt, Huấn luyện Model Đa mô hình (Random Forest, XGBoost, SVR, Ensemble) và Tối ưu hóa Siêu tham số an toàn (chống Data Leakage).

## Hướng Dẫn Cài Đặt và Chạy

Để chạy lại toàn bộ pipeline, cần môi trường Python (khuyến nghị Python 3.8+) và thực hiện các bước sau:

### Bước 1: Clone Repository

Tải source code về máy:

```bash
git clone https://github.com/uyen-huynh2808/predict-house-price FINAL_PROJECT_DS_K23
cd FINAL_PROJECT_DS_K23
```

### Bước 2: Chuẩn bị Môi trường (Environment Setup)
Tạo và kích hoạt môi trường ảo (Virtual Environment) để cô lập các thư viện:

```bash
# Tạo môi trường ảo
python -m venv venv

# Kích hoạt môi trường ảo (trên Windows)
.\venv\Scripts\activate
# Kích hoạt môi trường ảo (trên MacOS/Linux)
source venv/bin/activate
```

### Bước 3: Cài đặt Thư viện Phụ thuộc
Sử dụng file `requirements.txt` để cài đặt tất cả các thư viện cần thiết:

```bash
pip install -r requirements.txt
```

### Bước 4: Chạy Pipeline
Vì file dữ liệu thô (`rawdata.csv`) đã có sẵn trong thư mục `data/raw/`, chỉ cần chạy lệnh sau để khởi động toàn bộ quy trình:

```bash
python main.py --config config/config.yaml
```
> [Lưu ý] Sau khi chạy xong, kết quả đánh giá mô hình, biểu đồ và các file log sẽ được tạo tự động trong thư mục `models/` và `reports/figures/`.
