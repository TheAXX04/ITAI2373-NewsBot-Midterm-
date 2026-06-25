# ITAI2373-NewsBot-Midterm-
# NewsBot Intelligence System

ITAI 2373 - Mid-Term Group Project. An end to end NLP pipeline that classifies news
articles, extracts named entities, and analyzes sentiment across six categories.

## Files
- `Midterm_NewsBot_Intelligence_System_COMPLETE.ipynb` — the full notebook (all 8 modules)
- `news_dataset.csv` - 120 labeled news articles (20 each across 6 categories)
- `requirements.txt` - Python dependencies

## Dataset
120 BBC-style articles, balanced across **Politics, Sports, Technology, Business,
Entertainment, Health**. Columns: `article_id, title, content, category, date, source`.

## How to Run (VS Code)
1. Open the folder in VS Code with the Python + Jupyter extensions installed.
2. Open the notebook and select a Python 3 kernel (top-right).
3. Run the **Setup** cell once it installs packages, downloads the spaCy model
   `en_core_web_sm`, and fetches NLTK data.
4. Run all remaining cells top to bottom. Keep `news_dataset.csv` in the same folder.

## Modules
1. NLP context & data exploration
2. Text preprocessing (clean, tokenize, lemmatize)
3. TF-IDF feature extraction + word clouds/heatmaps
4. POS tagging & grammatical profiles
5. Dependency parsing & syntactic complexity
6. Sentiment analysis (VADER)
7. Text classification (Naive Bayes, Logistic Regression, SVM) + tuning
8. Named Entity Recognition + co-occurrence

## Results
~0.83 test accuracy (Naive Bayes) on the 6-class task. Note: combined features are
scaled with `MaxAbsScaler` so length features don't overwhelm TF-IDF.
