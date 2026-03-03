# Financial News Sentiment & Stock Market Direction Prediction

**Course Project | NLP Course**  
**Team:** Ajai Shakya, Reem Ahmed, Srivarshini Ankaiah Krishnappa

---

## Project Overview
This project investigates whether sentiment extracted from daily financial news 
headlines can predict the direction of the Dow Jones Industrial Average (DJIA). 
We compare a general-purpose sentiment tool (VADER) against a finance-specific 
transformer model (FinBERT), and evaluate their predictive power using Logistic 
Regression and Support Vector Machine classifiers.

---

## Dataset
- **Source:** Kaggle — [Daily News for Stock Market Prediction](https://www.kaggle.com/datasets/aaron7sun/stocknews)
- **File:** `Combined_News_DJIA.csv`
- **Size:** ~2,000 trading days, 25 headlines per day
- **Label:** Binary — DJIA closed Up (1) or Down (0)

> The dataset is not included in this repo due to size. Download it from Kaggle 
> and place it in the `/data` folder.

---

## Models Used
| Model | Type | Purpose |
|---|---|---|
| VADER | Lexicon-based | General sentiment scoring |
| FinBERT | Transformer (BERT-based) | Finance-specific sentiment scoring |
| Logistic Regression | Classifier | Market direction prediction |
| SVM | Classifier | Market direction prediction |

---

## Project Structure
```
├── data/                          # Place Kaggle CSV here (not tracked by Git)
├── notebooks/
│   ├── 01_eda.ipynb               # Exploratory data analysis
│   ├── 02_preprocessing.ipynb     # Tokenization, cleaning, stopword removal
│   ├── 03_vader_sentiment.ipynb   # VADER sentiment scoring
│   ├── 04_finbert_sentiment.ipynb # FinBERT sentiment scoring
│   └── 05_classification.ipynb   # LR, SVM, evaluation metrics
├── src/
│   ├── preprocess.py              # Reusable preprocessing functions
│   ├── sentiment.py               # VADER and FinBERT scoring functions
│   └── evaluate.py                # Evaluation and visualization functions
├── results/                       # Saved outputs, charts, metric tables
├── requirements.txt               # Python dependencies
└── README.md
```

---

## Setup Instructions
1. Clone the repository
```bash
git clone https://github.com/[your-username]/[your-repo-name].git
cd [your-repo-name]
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Download the dataset from Kaggle and place `Combined_News_DJIA.csv` in the `/data` folder

4. Run notebooks in order starting from `01_eda.ipynb`

---

## Team Responsibilities
| Member | Responsibility |
|---|---|
| Ajai Shakya | Data preprocessing & exploratory data analysis |
| Reem Ahmed | VADER & FinBERT sentiment extraction |
| Srivarshini Ankaiah Krishnappa | Classification models & evaluation |

---

## Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- Same-day and lagged (t+1, t+2) sentiment-market correlation analysis

---

## References
Full annotated bibliography available in the project proposal document.
```

---

## Step 3: Create the folder structure
GitHub won't let you create empty folders, so you need a placeholder file in each one. After your README is saved, do this:

**For each folder, click "Add file" → "Create new file" and name it exactly like this:**

| Type in the filename box | What it creates |
|---|---|
| `data/.gitkeep` | data folder |
| `notebooks/.gitkeep` | notebooks folder |
| `src/.gitkeep` | src folder |
| `results/.gitkeep` | results folder |

For each one, scroll down and click **"Commit new file"** with the default message.

---

## Step 4: Add a .gitignore
Click "Add file" → "Create new file," name it `.gitignore`, and paste this inside:
```
# Dataset (too large for GitHub)
data/*.csv

# Python
__pycache__/
*.pyc
.ipynb_checkpoints/

# Environment
.env
venv/
```

Commit it. This prevents the Kaggle CSV and notebook checkpoints from being accidentally uploaded.

---

## Step 5: Add requirements.txt
Click "Add file" → "Create new file," name it `requirements.txt`, paste this:
```
pandas
numpy
nltk
vaderSentiment
transformers
torch
scikit-learn
matplotlib
seaborn
jupyter
