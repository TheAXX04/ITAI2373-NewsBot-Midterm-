# 🤖 NewsBot Intelligence System
ITAI 2373 — Mid-Term Group Project. An end-to-end NLP pipeline that classifies news
articles, extracts named entities, and analyzes sentiment.

## 📊 Dataset (Kaggle — real data)
This notebook uses a real BBC News dataset. Recommended: the **learn-ai-bbc**
competition's `BBC News Train.csv` (1,490 articles, 5 categories: business,
entertainment, politics, sport, tech).

Meets the project requirements: ≥500 articles, ≥4 categories, full article text,
clear labels, English.

### How to download (VS Code, no Colab needed)
**Easiest — manual download:**
1. Go to https://www.kaggle.com/competitions/learn-ai-bbc/data
2. Sign in (free Kaggle account) and accept the competition rules.
3. Download `BBC News Train.csv`.
4. Put that CSV in the SAME folder as this notebook (or in your Downloads folder).
5. Run the notebook — the loader auto-detects it.

**Optional — Kaggle API (VS Code terminal):**
```bash
pip install kaggle
# Put kaggle.json at: C:\Users\<You>\.kaggle\kaggle.json  (Windows)
#                 or: ~/.kaggle/kaggle.json                (Mac/Linux)
kaggle competitions download -c learn-ai-bbc      # must accept rules on site first
# unzip the downloaded file, keep "BBC News Train.csv" next to the notebook
```

The loader also works with these alternatives automatically:
- `bbc-text.csv` (yufengdev/bbc-fulltext-and-category)
- `bbc-news-data.csv` (hgultekin/bbcnewsarchive, tab-separated)
- the included synthetic `news_dataset.csv`

## 🚀 Run (VS Code)
1. Open the folder in VS Code (Python + Jupyter extensions installed).
2. Open the notebook, select a Python 3 kernel.
3. Run the **Setup** cell once (installs packages + spaCy `en_core_web_sm` + NLTK data).
4. Run all cells top to bottom.

## 🧩 Modules
Preprocessing → TF-IDF → POS tagging → dependency parsing → sentiment (VADER) →
classification (Naive Bayes / Logistic Regression / SVM + tuning) → NER + co-occurrence.

## 📈 Notes
- Combined features are scaled with `MaxAbsScaler` so length features don't overwhelm TF-IDF.
- Expect ~95–97% accuracy on the real BBC dataset.
