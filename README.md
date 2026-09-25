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
- Hiểu Neural Network, MLP và CNN
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

Mỗi ảnh trong dataset:

```text
28 × 28 pixels
```

Tương ứng:

```text
784 pixel features
```

Label là chữ số từ:

```text
0 → 9
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
python -m pip install -r requirements.txt
```

Các thư viện chính được sử dụng trong project:

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow / Keras

TensorFlow được sử dụng từ giai đoạn Neural Network, MLP và CNN.

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
git checkout -b feature/step-23-cnn-baseline
```

### Sau khi hoàn thành

```bash
git status
git add .
git commit -m "Add CNN baseline"
git push -u origin feature/step-23-cnn-baseline
```

Quy trình:

```text
Pull main mới nhất
        ↓
Tạo branch riêng
        ↓
Code / Experiment
        ↓
Commit
        ↓
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
| 4–15 | ML fundamentals + Logistic Regression | Done |
| 16–20 | Neural Network + MLP | Done |
| 21–22 | Chuẩn bị kiến thức Computer Vision / CNN | Done |
| 23 | CNN baseline | In Progress |
| 24–26 | CNN evaluation + improvement | Not Started |
| 27 | So sánh các model | Not Started |
| 28–30 | Inference + Kaggle Submission | Not Started |
| 31–34 | Results + README + Cleanup | Not Started |

---

## Các model

### Logistic Regression

Model baseline đầu tiên của project.

Các nội dung đã thực hiện:

- Chia train / validation
- Normalize dữ liệu
- Train Logistic Regression
- Đánh giá train accuracy và validation accuracy
- Phân tích generalization và overfitting
- Confusion Matrix
- Phân tích các cặp chữ số dễ bị dự đoán nhầm

---

### Multi-Layer Perceptron

Neural Network đầu tiên của project.

Các nội dung đã thực hiện:

- Xây dựng MLP bằng TensorFlow / Keras
- Dense layers
- ReLU activation
- Softmax output
- Forward propagation
- Loss
- Backpropagation
- Optimizer
- Train và validation accuracy
- Thử nghiệm thay đổi kiến trúc MLP

---

### Convolutional Neural Network

Giai đoạn hiện tại của project.

CNN nhận input dưới dạng:

```text
28 × 28 × 1
```

thay vì vector:

```text
784
```

Kiến trúc baseline:

```text
Input Image
    ↓
Conv2D
    ↓
ReLU
    ↓
MaxPooling2D
    ↓
Flatten
    ↓
Dense
    ↓
Softmax
    ↓
10 classes
```

Mục tiêu:

- Hiểu convolution
- Hiểu filter / kernel
- Hiểu feature map
- Hiểu pooling
- Hiểu cách CNN giữ thông tin không gian của ảnh
- Xây dựng CNN baseline
- Đánh giá CNN trên validation set

---

## Kết quả model

| Model | Validation Accuracy | Kaggle Score | Status |
|---|---:|---:|---|
| Logistic Regression | — | — | Done |
| MLP | — | — | Done |
| CNN | — | — | In Progress |

Các giá trị accuracy và Kaggle score sẽ được cập nhật từ kết quả thực tế trong notebook.

---

## Thành viên

| Thành viên | Vai trò |
|---|---|
| Kiệt | Development / Experiment / Review |
| Sơn | Development / Experiment / Review |

Hai thành viên luân phiên vai trò **driver** và **reviewer** trong từng bước của project.

---

## Trạng thái hiện tại

Đã hoàn thành:

```text
Data Exploration
        ↓
Logistic Regression
        ↓
Generalization / Overfitting
        ↓
Model Evaluation
        ↓
Neural Network Fundamentals
        ↓
MLP
```

Hiện tại:

```text
Step 23
CNN Baseline
```

Đang thực hiện:

```text
MNIST image
28 × 28 × 1
      ↓
   Conv2D
      ↓
MaxPooling2D
      ↓
   Flatten
      ↓
    Dense
      ↓
10-class prediction
```

Mục tiêu của Step 23:

- Chuẩn bị dữ liệu cho CNN
- Reshape `784 → 28 × 28 × 1`
- Hiểu `Conv2D`
- Hiểu filter và kernel
- Hiểu `MaxPooling2D`
- Hiểu `Flatten`
- Xem `model.summary()`
- Xây dựng và train CNN baseline đầu tiên

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