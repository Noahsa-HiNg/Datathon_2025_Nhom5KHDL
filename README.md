# 📦 Datathon 2026 — Submission Repository  
## Team: KHDL Nhóm 5

---

## 1. Kaggle Submission

- File nộp: `submission.csv`
- Yêu cầu:
  - Đúng số dòng
  - Đúng thứ tự như `sample_submission.csv`
  - Không có giá trị thiếu (NaN)

---

## 2. Báo cáo (PDF)

- Sử dụng template **LaTeX NeurIPS**
- Tối đa **4 trang** không tính references và appendix

### Nội dung báo cáo bao gồm:

- Trực quan hoá và phân tích dữ liệu (**Phần 2 — EDA**)
- Pipeline mô hình và phương pháp dự báo (**Phần 3 — Forecasting**)
- Kết quả thực nghiệm và phương pháp đánh giá
- Link GitHub repository

---

## 3. Repository Structure

Repository bao gồm toàn bộ code, notebook phân tích, notebook mô hình và file submission.

```text
.
├── data/
├── notebooks/
│   ├── 01_mcq_answers.ipynb
│   ├── 02_eda_dashboard_final.ipynb
│   └── 03_forecasting_model.ipynb
├── outputs/
│   └── figures/
├── submission.csv
└── README.md
```

---

## 4. Reproducibility

### Cài đặt môi trường

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

### Chạy lại kết quả

Chạy các notebook theo thứ tự:

```text
1. notebooks/02_eda_dashboard_final.ipynb
2. notebooks/03_forecasting_model.ipynb
```

---

## 5. Methodology

### 5.1. Exploratory Data Analysis — Phần 2

Phân tích EDA được thực hiện theo các mảng kinh doanh chính:

- Revenue & Seasonality
- Customer & Retention
- Product & Profitability
- Promotion Effectiveness
- Returns & Customer Experience
- Inventory & Operations
- Web Traffic & Conversion

Khung phân tích sử dụng trong dashboard:

```text
Descriptive → Diagnostic → Predictive → Prescriptive
```

Mục tiêu của phần EDA là không chỉ mô tả dữ liệu, mà còn tìm ra nguyên nhân, cảnh báo rủi ro và đề xuất hành động kinh doanh có thể áp dụng.

---

### 5.2. Forecasting — Phần 3

- Mục tiêu: dự báo **Revenue theo ngày**
- Dữ liệu chính: `sales.csv`

#### Validation Strategy

Do dữ liệu có sự thay đổi theo thời gian, nhóm sử dụng **time-based hold-out validation**:

```text
Train: 2012 – 2021
Validation: 2022
```

Nhóm không sử dụng cross-validation trên toàn bộ dữ liệu để tránh sai lệch do khác biệt phân phối giữa các giai đoạn.

#### Mô hình sử dụng

- Seasonal Naive
- Rolling Average
- Gradient Boosting
- Final Ensemble

Cách tiếp cận kết hợp:

- Phương pháp thống kê để nắm bắt trend và seasonality
- Machine Learning để học các pattern phi tuyến
- Ensemble để cải thiện độ ổn định và giảm sai số dự báo

---

## 6. Reproducibility Notes

- Không sử dụng dữ liệu ngoài
- Code có thể chạy lại toàn bộ
- Có sử dụng random seed khi cần thiết
- Các file notebook, figures và `submission.csv` được lưu trong repository

---

## 7. Evaluation Notes

- Kaggle được sử dụng để đánh giá trên tập test ẩn
- Các chỉ số MAE, RMSE và R² được tính trên tập validation năm 2022
- File `submission.csv` giữ đúng cấu trúc và thứ tự dòng của `sample_submission.csv`

---

## 8. Links

- Kaggle Submission: https://drive.google.com/file/d/1CFD-h6ZUv5yienL1u6pXzC6mImaV3eq2/view?usp=drive_link
- GitHub Repository: https://github.com/Noahsa-HiNg/Datathon_2025_Nhom5KHDL

---

# Completed