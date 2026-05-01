# Datathon 2026 Round 1

Repository này chứa toàn bộ notebook phân tích, notebook mô hình và dữ liệu dùng cho bài toán Datathon 2026 Round 1 của nhóm KHDL Nhóm 5.

## Nội dung chính

- EDA và dashboard trực quan nằm trong [02_eda_dashboard_final.ipynb](02_eda_dashboard_final.ipynb)
- Phân tích dữ liệu chi tiết nằm trong [data_eda.ipynb](data_eda.ipynb)
- Xây dựng mô hình dự báo nằm trong [Model.ipynb](Model.ipynb)
- Notebook thử nghiệm/triển khai từng phần nằm trong [part1.ipynb](part1.ipynb)
- Notebook baseline gốc của cuộc thi nằm trong [datathon-2026-round-1/baseline.ipynb](datathon-2026-round-1/baseline.ipynb)

## Cấu trúc thư mục

```text
.
├── 02_eda_dashboard_final.ipynb
├── data_eda.ipynb
├── Model.ipynb
├── part1.ipynb
├── README.md
├── datathon-2026-round-1/
│   ├── baseline.ipynb
│   ├── customers.csv
│   ├── geography.csv
│   ├── inventory.csv
│   ├── order_items.csv
│   ├── orders.csv
│   ├── payments.csv
│   ├── products.csv
│   ├── promotions.csv
│   ├── returns.csv
│   ├── reviews.csv
│   ├── sales.csv
│   ├── sample_submission.csv
│   ├── shipments.csv
│   └── web_traffic.csv
└── submission/
    └── submission.csv
```

## Dữ liệu

Bộ dữ liệu cuộc thi được lưu trong thư mục [datathon-2026-round-1](datathon-2026-round-1) và gồm nhiều bảng liên kết theo nghiệp vụ bán hàng, khách hàng, tồn kho, vận chuyển, đánh giá và lưu lượng web.

Các file quan trọng nhất khi tạo kết quả nộp là:

- [datathon-2026-round-1/sample_submission.csv](datathon-2026-round-1/sample_submission.csv)
- [submission/submission.csv](submission/submission.csv)

## Cách chạy lại

1. Mở notebook theo đúng thứ tự cần phân tích hoặc mô hình hoá.
2. Chạy lại các cell với cùng môi trường Python đang dùng trong dự án.
3. Sau khi sinh dự đoán, xuất file nộp vào [submission/submission.csv](submission/submission.csv).

Nếu cần cài nhanh các thư viện cơ bản cho notebook, có thể dùng:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly
```

## Ghi chú

- Không nên phụ thuộc vào đường dẫn cũ như `data/`, `notebooks/` hay `outputs/` vì chúng không còn khớp với workspace hiện tại.
- File [datathon-2026-round-1/sample_submission.csv](datathon-2026-round-1/sample_submission.csv) nên được dùng làm mẫu để đảm bảo đúng số dòng và đúng thứ tự khi tạo submission.
