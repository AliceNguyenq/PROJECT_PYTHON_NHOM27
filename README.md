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


## 📁 Cấu trúc Project


project/
│
├─ 📁 Result/                                      # Kết quả mô hình & log quá trình chạy
│   ├── result_grid.csv                            # Kết quả GridSearchCV – tham số tối ưu
│   ├── result_random.csv                          # Kết quả RandomSearchCV
│   ├── training.log                               # Log quá trình training (pipeline + model)
│ 
├─ 📁 data train cleaned/                           # Dữ liệu TRAIN đã làm sạch 
│   ├── clean_user.csv                     # User train 
│   ├── clean_context.csv                  # Context train 
│   ├── clean_mobile_plan_user.csv         # Lịch sử gói cước (train)
│   ├── clean_mobile_plan_attr.csv         # Mô tả gói cước (train)
│   ├── data_train_cleaned.csv                   # Dataset cuối huấn luyện mô hình
│   ├── mobile_plan_user_agg.csv                   # Dataset tổng hợp từ file clean_mobile_plan_user.csv
│   └── (Tổng cộng: 6 file CSV)
│
├─ 📁 data test cleaned/                            # Dữ liệu TEST đã làm sạch
│   ├── clean_user_test.csv
│   ├── clean_context_test.csv
│   ├── clean_mobile_plan_user_test.csv
│   ├── clean_mobile_plan_attr_test.csv
│   ├── data_test_cleaned.csv
│   ├── mobile_plan_user_agg_test.csv
│   └── (Tổng cộng: 6 file CSV)
│
├─ 📁 train data/                                   # Dữ liệu TRAIN thô (raw)
│   ├── user.csv                                     # Thông tin nhân khẩu học ban đầu
│   ├── context.csv                                  # Thông tin chuyến đi ban đầu
│   ├── mobile_plan_user.csv                         # Gói cước đề xuất/đã chọn (raw)
│   ├── mobile_plan_attr.csv                          # Thông tin gói data (raw)
│   └── (4 file CSV)
│
├─ 📁 test data/                                    # Dữ liệu TEST thô (raw)
│   ├── user_test.csv
│   ├── context_test.csv
│   ├── mobile_plan_user_test.csv
│   ├── mobile_plan_attr_test.csv
│   └── (4 file CSV)
│
├─ 📁 notebooks/                                    # Notebook phân tích & xây dựng mô hình
│   ├── [NHOM27_PYTHON_1]_DataPreprocessing_NoneClass.ipynb    # Xử lý dữ liệu không sử dụng class
│   ├── [NHOM27_PYTHON_2]_DataPreprocessing_WithClass.ipynb    # Xử lý dữ liệu có sử dụng class
│   ├── [NHOM27_PYTHON_3]_EDA.ipynb                            # Phân tích dữ liệu (EDA)
│   ├── [NHOM27_PYTHON_4]_Model_Final.ipynb                    # Huấn luyện & đánh giá mô hình
│
├─ 📄 [NHOM27_PYTHON_5]_Report_File.pdf             # Báo cáo chính thức
├─ 📄 LICENSE                                       # Giấy phép MIT License
├─ 📄 requirements.txt                              # Danh sách thư viện phụ thuộc Python
└─ 📄 README.md                                     # Mô tả project



## Prerequisites
Trước khi bắt đầu, hãy đảm bảo đã đáp ứng các yêu cầu sau:
- Phiên bản Python >= 3.8
- Các thư viện cần thiết được liệt kê trong requirements.txt (bao gồm: pandas, numpy, scikit-learn, xgboost, lightgbm, catboost, seaborn, matplotlib, joblib, …)
- (Tùy chọn) Công cụ được đề xuất:
     + Jupyter Notebook / VSCode để chạy các notebook định dạng .ipynb
     + Môi trường ảo (venv/conda) để cô lập các phụ thuộc
 

##  Cách cài đặt 
1. Sao chép (clone) kho lưu trữ này về máy của bạn:
   ```bash
   git clone https://github.com/AliceNguyenq/PROJECT_PYTHON_NHOM27.git
   ```
2. Di chuyển đến thư mục của dự án:
   ```bash
   cd PROJECT_PYTHON_NHOM27
   ```
3. (Khuyến nghị) Tạo môi trường ảo:
- Windows:
  ```bash
  python -m venv venv
  venv\Scripts\activate
   ```
- macOS / Linux:
  ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
4. Cài đặt các thư viện/phụ thuộc cần thiết:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
Sử dụng notebook để chạy từng bước phân tích:
- Mở Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
- Các notebook chính:

| Notebook                                              | Chức năng                                     |
| ----------------------------------------------------- | --------------------------------------------- |
| `[NHOM27_PYTHON_1]_DataPreprocessing_NoneClass.ipynb` | Tiền xử lý dữ liệu không sử dụng class        |
| `[NHOM27_PYTHON_2]_DataPreprocessing_WithClass.ipynb` | Tiền xử lý dữ liệu có sử dụng class           |
| `[NHOM27_PYTHON_3]_EDA.ipynb`                         | Phân tích dữ liệu khám phá (EDA)              |
| `[NHOM27_PYTHON_4]_Model_Final.ipynb`                 | Xây dựng, huấn luyện, đánh giá mô hình        |

  
> [Lưu ý] Sau khi chạy xong, kết quả đánh giá mô hình và file log sẽ được tạo tự động.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
