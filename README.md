# 🎬 Movie Review Sentiment Analyzer

Ever wondered if a machine can tell whether a movie review is full of love ❤️ or pure hate 💔?
This project does exactly that! It’s a simple, end-to-end sentiment analysis pipeline that takes in raw IMDB movie reviews and predicts whether they’re positive or negative.

At its core, it uses TF-IDF vectorization to turn words into numbers and a Logistic Regression classifier to make the final call. Clean, reproducible, and beginner-friendly 🚀.

## ✨ Features

- Loads IMDB reviews straight from a CSV file (review, sentiment)

- Handles text column aliases (auto-renames to review)

- Text vectorization using TF-IDF with scikit-learn

- Classification with Logistic Regression (liblinear solver)

- Evaluation with Accuracy, F1-score, Confusion Matrix, and Classification Report

- End-to-end workflow in a single notebook — no missing pieces

## 📂 Project Structure

- Movie_Review_Sentiment_Analyzer.ipynb → The main notebook (all steps included)

- IMDB Dataset.csv → Input dataset (50,000 labeled reviews)

## 🛠️ Requirements

- Python 3.8+

- pandas

- numpy

- scikit-learn

## 👉 Install everything at once:

pip install -r requirements.txt


Example requirements.txt:

- pandas
- numpy
- scikit-learn

## 📑 Dataset Format

The project expects a file named IMDB Dataset.csv with:

- review (or text) → the actual review

- sentiment → target label: positive or negative

**Notes:**

- Column names are normalized to lowercase.

- If review is missing but text exists, it’s renamed.

- Missing values are dropped automatically.

## ⚙️ How It Works

- Import libraries (pandas, numpy, scikit-learn)

- Load dataset & clean column names

- Validate required columns (review, sentiment)

- Train-test split

- Convert text → TF-IDF features

- Train Logistic Regression classifier

- Evaluate with accuracy, F1-score, confusion matrix & classification report

## 🚀 Usage

- Place IMDB Dataset.csv in the same folder as the notebook.

- Open Movie_Review_Sentiment_Analyzer.ipynb in Jupyter or VS Code.

- Run all cells → Done! 🎉

💡 Want to use your own dataset? Just make sure your CSV has review (or text) + sentiment (positive/negative).

## 🔧 Customization

- Vectorizer → tweak ngram_range, min_df, max_df, or add stop_words

- Model → tune Logistic Regression (C, solver, class_weight, max_iter)

- Split → adjust test_size or random_state

- Preprocessing → add steps like lowercasing, punctuation removal, emoji handling 😎

## 📊 Outputs

- Console metrics: accuracy, F1-score

- Confusion Matrix

- Detailed classification report (per class)

## 🐞 Common Issues & Fixes

- FileNotFoundError → Make sure IMDB Dataset.csv is in the same directory

- Column Errors → Check for review (or text) + sentiment

- ConvergenceWarning → Increase max_iter or adjust C/solver

- Typo Fix → Use df.dropna(...), not df.dropa(...)

## 📜 License

Pick your favorite (MIT recommended).
