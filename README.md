# Movie-Review-Sentiment-Analyzer
A simple, end-to-end sentiment analysis project that classifies IMDB movie reviews as positive or negative using TF-IDF features and Logistic Regression. This project loads a CSV dataset, performs basic validation, vectorizes text, trains a classifier, and evaluates performance with common metrics.

## Features
- *Loads IMDB reviews from a CSV file with columns: review, sentiment

- *Accepts text column alias: text (auto-renamed to review)

- *TF-IDF vectorization with scikit-learn

- *Logistic Regression classifier (liblinear)

- *Metrics: accuracy, F1-score, confusion matrix, classification report

- *Clean, reproducible training/evaluation pipeline

## Project Structure
- *Movie_Review_Sentiment_Analyzer.ipynb — Main notebook containing the full workflow

- *IMDB Dataset.csv — Expected input dataset (50,000 labeled reviews)

## Requirements
- *Python 3.8+

- *pandas

- *numpy

- *scikit-learn

## Dataset Format
The notebook expects a CSV file named IMDB Dataset.csv in the working directory with:

- *review (or text) — the review text

- *sentiment — target label: positive or negative

**Notes:**

- *The notebook normalizes column names to lowercase.

_ *If review is missing but text exists, it is renamed to review.

- *The code validates presence of review and sentiment.

## How It Works
- *Import libraries (pandas, numpy, scikit-learn)

- *Load the IMDB dataset CSV and normalize column names

- *Validate required columns; drop missing values

- *Split data into train and test sets

- *Transform text using TfidfVectorizer

- *Train LogisticRegression

- *Evaluate with accuracy, F1, confusion matrix, and classification report

## Usage
- 1.Place IMDB Dataset.csv alongside the notebook.

- 2.Open Movie_Review_Sentiment_Analyzer.ipynb in Jupyter or VS Code.

 3.Run all cells to train and evaluate the model.

Tip:

To adapt for a different dataset, ensure the CSV has columns review (or text) and sentiment with values positive/negative.

Customization
Vectorizer: Adjust TfidfVectorizer parameters (e.g., ngram_range, min_df, max_df, stop_words)

Model: Tune LogisticRegression hyperparameters (C, solver, class_weight, max_iter)

Split: Change test_size or random_state in train_test_split

Preprocessing: Add cleaning steps (lowercasing, punctuation removal) before vectorization if desired

Outputs
Console metrics: accuracy_score, f1_score

Confusion matrix

Detailed classification_report per class

Common Issues and Fixes
FileNotFoundError: Ensure IMDB Dataset.csv is in the same directory as the notebook.

Column errors: Confirm presence of review (or text) and sentiment columns.

ConvergenceWarning: Increase max_iter or adjust C/solver.

Typo in code: Replace df.dropa(...) with df.dropna(...) to drop missing values.

Correct line:

df = df.dropna(subset=['review', 'sentiment']).reset_index(drop=True)

Roadmap
Add train/val/test split and cross-validation

Persist model and vectorizer via joblib

Add preprocessing pipeline (HTML tag removal, contractions, emojis)

Handle class imbalance (class_weight or resampling)

Provide CLI and FastAPI/Flask inference endpoint

Add unit tests and CI

License
Specify a license (e.g., MIT) in LICENSE.
