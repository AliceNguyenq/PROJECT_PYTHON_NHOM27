# PROJECT_PYTHON_NHOM27

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)


## Description
Đây là một dự án Python để phân tích dữ liệu khách hàng và xây dựng mô hình máy học dự đoán gói dịch vụ viễn thông
Mục tiêu của dự án là:
- Phân tích dữ liệu khách hàng và dữ liệu hành trình của du khách quốc tế đến Việt Nam.
- Xây dựng mô hình Multi-class Classification dự đoán gói cước 4G Viettel phù hợp cho từng khách hàng.

## Dataset
Dự án gồm 4 bảng dữ liệu chính:
user.csv	- Thông tin nhân khẩu học người dùng	- 11,572 × 16
context.csv	- Thông tin chuyến đi -	11,572 × 12
mobile_plan_user.csv	- Gói cước được đề xuất và lựa chọn của khách hàng -	45,321 × 3
mobile_plan_attr.csv	- Thông tin chi tiết các gói data Viettel	- 5 × 4


📁 project/
│
├─ 📁 Result/
├─ 📁 data test cleaned/
├─ 📁 data train cleaned/
├─ 📁 notebookooks/          # Có thể đổi tên: notebooks/
├─ 📁 test data/
├─ 📁 train data/
│
├─ 📄 LICENSE
├─ 📄 README.md
│
├─ 📄 [NHOM27_PYTHON_1]_DataPreprocessing_No...
├─ 📄 [NHOM27_PYTHON_2]_DataPreprocessing_With...
├─ 📄 [NHOM27_PYTHON_3]_EDA.ipynb
├─ 📄 [NHOM27_PYTHON_4]_Model_Final.ipynb
└─ 📄 [NHOM27_PYTHON_5]_Report_File.pdf




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
