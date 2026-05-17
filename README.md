# Wafer Defect Pattern Classifier

A machine learning pipeline that classifies semiconductor wafer defects
using real fabrication sensor data across 5 process steps. Built to mirror
the kind of predictive quality analytics used in semiconductor manufacturing.

---

## Results
- 99.9% classification accuracy using Random Forest
- Resolved extreme class imbalance (0.1% defect rate) using SMOTE
- 3-table SQL lot traceability schema linking wafers, measurements, and defect outcomes

---

## Tools & Libraries
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib
- Seaborn
- SQLite3 (built-in)

---

## Dataset
**Semiconductor Wafer Defect Classification Dataset**
- Source: [Kaggle](https://www.kaggle.com/datasets/meruvakodandasuraj/semiconductor-wafer-defect-classification-dataset)
- 5,000 wafer records
- 7 process parameters: temperature, pressure, gas flow, etch rate, voltage, current, process step
- Binary defect label: 0 = Normal, 1 = Defect

---

## Setup & Running Instructions

### Option 1 — Google Colab (Recommended)

1. Open the notebook directly in Google Colab:
   - Go to [colab.research.google.com](https://colab.research.google.com)
   - Click **File → Open Notebook → GitHub**
   - Paste this repository URL and select `wafer_defect_classifier.ipynb`

2. Download the dataset:
   - Go to the [Kaggle dataset page](https://www.kaggle.com/datasets/meruvakodandasuraj/semiconductor-wafer-defect-classification-dataset)
   - Click **Download**
   - Upload `semiconductor_wafer_defect_dataset.csv` to Colab using the
     left sidebar folder icon → Upload

3. Install the one library not pre-installed on Colab:
   #!pip install imbalanced-learn --quiet
   
4. Run all cells in order:
   - **Runtime → Run all**

---

### Option 2 — Local Setup

1. Clone the repository:
  git clone https://github.com/your-username/wafer-defect-classifier.git
  cd wafer-defect-classifier

2. Create a virtual environment (recommended):
   python -m venv venv
  source venv/bin/activate        # Mac/Linux
  venv\Scripts\activate           # Windows

3. Install all required libraries:
   # pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn jupyter

4. Download the dataset from Kaggle and place
   `semiconductor_wafer_defect_dataset.csv` in the project root folder.

5. Launch Jupyter Notebook:
   #jupyter notebook

6. Open `wafer_defect_classifier.ipynb` and run all cells in order.

---

## Project Structure
wafer-defect-classifier/
│
├── wafer_defect_classifier.ipynb   # Main notebook
├── semiconductor_wafer_defect_dataset.csv  # Dataset
└── README.md
---

## Notebook Structure
| Section | Description |
|---|---|
| 1. Load Dataset | Load and inspect raw sensor CSV |
| 2. EDA | Visualise defect patterns across process parameters |
| 3. SMOTE | Fix class imbalance before training |
| 4. Model Training | Train Random Forest classifier |
| 5. Evaluation | Classification report, confusion matrix, feature importance |
| 6. SQL Schema | Lot traceability database design |

---

## Author
Sharon Lee (I build projects when I have nothing to do, yes I am insane)
[LinkedIn](https://www.linkedin.com/in/sharon-jia-yi-lee-211251358)
