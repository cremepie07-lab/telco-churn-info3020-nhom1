# INFO3020 – Telco Customer Churn (Nhóm 1)

Báo cáo giữa kỳ môn Khoa học dữ liệu: phân tích khách hàng rời bỏ (churn) của một công ty viễn thông trên bộ dữ liệu IBM Telco (7,043 khách × 21 cột).

**Câu hỏi nghiên cứu:** Nhóm khách hàng nào (theo loại hợp đồng, dịch vụ internet, thời gian sử dụng) có tỷ lệ churn cao nhất, và chênh lệch lớn đến mức nào?

## Kết quả chính
- Tỷ lệ churn chung: **26.5%** (1,869 / 7,043 khách).
- Hợp đồng tháng **42.7%** so với hợp đồng 2 năm **2.8%**.
- Fiber optic **41.9%**; Fiber + hợp đồng tháng **54.6%**.
- Khách 0–12 tháng **47.4%**; khoảng 55% khách churn rời đi trong 12 tháng đầu.
- Đây là **tương quan, không phải nhân quả**.

## Cấu trúc thư mục
```
notebook/   giua_ky_full_da_sua.ipynb + file CSV (đặt cùng thư mục, notebook đọc tên file gốc)
figures/    6 hình xuất ra từ notebook (histogram + 5 biểu đồ chính)
report/     báo cáo Word (.docx)
```

## Cách chạy
```bash
pip install -r requirements.txt
cd notebook
jupyter notebook giua_ky_full_da_sua.ipynb   # chọn Restart & Run All
```
Notebook lưu hình `.png` ngay trong `notebook/`; bản đã chạy sẵn nằm ở `figures/`.

## Dữ liệu
IBM Sample Dataset – Telco Customer Churn: https://www.kaggle.com/datasets/blastchar/telco-customer-churn (snapshot một thời điểm, một dòng = một khách hàng).

## Thành viên và phân công
| # | Họ tên – MSSV | GitHub | Phần phụ trách |
|---|---|---|---|
| 1 | [..] | @[..] | Phần 1–2: context, data dictionary; tổng hợp báo cáo |
| 2 | [..] | @[..] | Phần 3: cleaning log |
| 3 | [..] | @[..] | Phần 4.1–4.2: thống kê mô tả, phân tích theo nhóm; biểu đồ 1–2 |
| 4 | [..] | @[..] | Phần 4.3–4.4, 5–6: biểu đồ 3–5, confounder, findings, limitations |

## Quy tắc làm việc nhóm
1. Không commit thẳng vào `main`. Mỗi người làm trên nhánh riêng: `feature/<ten>-<phan>` (ví dụ `feature/an-cleaning`).
2. Commit nhỏ, thông điệp rõ: `cleaning: điền 0 cho TotalCharges khi tenure = 0`.
3. Mở Pull Request vào `main`, ít nhất 1 bạn khác xem trước khi merge.
4. Trước khi sửa notebook, báo trong nhóm để tránh xung đột (file `.ipynb` rất khó gộp). Mỗi lần chỉ một người sửa notebook; sau khi sửa xong chạy *Restart & Run All*.
5. Báo cáo `.docx` cũng chỉ một người chỉnh tại một thời điểm.
