# MNIST Digit Recognition - Kaggle Project

> Dự án Machine Learning được thực hiện trong quá trình học ML và tham gia cuộc thi **Kaggle Digit Recognizer**.

---

## Mục tiêu

Project này được dùng để vừa học kiến thức Machine Learning, vừa áp dụng trực tiếp vào một bài toán thực tế.

Lộ trình model:

```text
Logistic Regression
        ↓
       MLP
        ↓
       CNN
        ↓
Kaggle Submission
```

Mục tiêu cuối cùng:

- Hiểu pipeline Machine Learning cơ bản
- Biết cách xử lý và trực quan hóa dữ liệu
- Xây dựng và đánh giá nhiều model
- So sánh Logistic Regression, MLP và CNN
- Tạo submission cho Kaggle
- Hoàn thiện project để đưa lên GitHub/portfolio

---

## Cấu trúc project

```text
AI-Kaggle/
│
├── data/               # Dataset local, không push lên GitHub
├── notebooks/          # Notebook học tập và experiment
├── src/                # Source code dùng lại
├── models/             # Model đã train
├── results/            # Biểu đồ, confusion matrix, kết quả
├── submissions/        # File submission Kaggle
│
├── .gitignore
├── README.md
└── requirements.txt
```

---

## Dataset

Project sử dụng dataset từ cuộc thi **Kaggle Digit Recognizer**.

Dataset **không được lưu trên GitHub**.

Sau khi tải từ Kaggle, đặt file vào:

```text
data/
├── train.csv
└── test.csv
```

---

## Cài đặt

### 1. Clone repository

```bash
git clone <repository-url>
cd AI-Kaggle
```

### 2. Tạo virtual environment

```bash
python -m venv .venv
```

### 3. Kích hoạt môi trường

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Cài thư viện

```bash
pip install -r requirements.txt
```

---

## Git Workflow

### Trước khi bắt đầu công việc mới

```bash
git checkout main
git pull origin main
```

### Tạo branch riêng

Ví dụ:

```bash
git checkout -b feature/step-05-data-inspection
```

### Sau khi hoàn thành

```bash
git status
git add .
git commit -m "Load and inspect dataset"
git push -u origin feature/step-05-data-inspection
```

Quy trình:

```text
Push branch
    ↓
Create Pull Request
    ↓
Người còn lại review
    ↓
Merge vào main
    ↓
Cả hai pull main mới nhất
```

---

## Quy ước làm việc nhóm

| Quy tắc | Nội dung |
|---|---|
| `main` | Không code trực tiếp |
| Branch | Mỗi task dùng một branch riêng |
| Pull | Luôn pull `main` trước khi tạo branch |
| Review | Người còn lại review trước khi merge |
| Notebook | Không cùng sửa một `.ipynb` tại cùng thời điểm |
| Dataset | Không push `train.csv`, `test.csv` |
| Environment | Không push `.venv` |
| Commit | Viết commit message rõ ràng bằng tiếng Anh |
| Code | Tên biến, function, branch dùng tiếng Anh |
| Kiến thức | Cả hai phải hiểu code trước khi merge |

---

## Lộ trình

| Giai đoạn | Nội dung | Trạng thái |
|---|---|:---:|
| 0 | Tạo project và repository | Done |
| 1 | README ban đầu | Done |
| 2 | Project structure | Done |
| 3 | Tải Kaggle dataset | Done |
| 4–15 | ML fundamentals + Logistic Regression | In Progress |
| 16–20 | Neural Network + MLP | Not Started |
| 21–26 | Computer Vision + CNN | Not Started |
| 27 | So sánh các model | Not Started |
| 28–30 | Inference + Kaggle Submission | Not Started |
| 31–34 | Results + README + Cleanup | Not Started |

---

## Models

| Model | Validation Accuracy | Kaggle Score | Status |
|---|---:|---:|---|
| Logistic Regression | — | — | Not Started |
| MLP | — | — | Not Started |
| CNN | — | — | Not Started |

Bảng này sẽ được cập nhật trong quá trình thực hiện project.

---

## Thành viên

| Thành viên | Vai trò |
|---|---|
| Kiệt | Development / Experiment / Review |
| Sơn | Development / Experiment / Review |

Hai thành viên luân phiên vai trò **driver** và **reviewer** trong từng bước của project.

---

## Trạng thái hiện tại

Đã hoàn thành **Step 3 — Project setup + Kaggle dataset**.

Tiếp theo:

```text
Step 4
Google ML Crash Course
Intro + Linear Regression
```

---

## Kết quả cuối cùng

Phần này sẽ được cập nhật sau khi project hoàn thành:

```text
Best Model:
Validation Accuracy:
Kaggle Score:
Kaggle Rank:
```

---

> Project được xây dựng với mục tiêu học tập. Mỗi experiment ưu tiên hiểu **tại sao model hoạt động** thay vì chỉ tối ưu leaderboard.