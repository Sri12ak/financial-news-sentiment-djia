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
