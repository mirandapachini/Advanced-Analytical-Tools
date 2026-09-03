# Advanced Analytical Tools — Text Mining & NLP Fundamentals

Three coursework notebooks covering the core building blocks of text mining and NLP: preprocessing, vector-space representation, and text classification — implemented from first principles rather than relying on a single black-box library.

## Notebooks

### Assignment 1 — Text Preprocessing & Similarity Fundamentals
**File:** `Assignment_1.ipynb`

- **Preprocessing pipeline:** tokenization (NLTK), stopword removal, and stemming (Porter Stemmer) applied to product review text
- **Edit distance:** implemented the Levenshtein edit-distance algorithm from scratch (dynamic programming) to measure string similarity between words (e.g., "algorithm" vs. "logarithm")
- **Bag-of-Words search:** built BoW vectors by hand for a query ("wireless noise cancelling headphones") against three candidate documents, then ranked documents by dot-product similarity to find the best match — a from-scratch mini search engine

### Assignment 2 — Vector Space Models & TF-IDF
**File:** `Assignment2.ipynb`

- **Count vs. TF-IDF vectorization:** compared raw word-count vectors to TF-IDF-weighted vectors across a small document set, showing how TF-IDF down-weights common words and highlights each document's distinctive terms
- **Cosine similarity & visualization:** computed cosine similarity between document and query vectors, visualized document vectors in 2D space, and built similarity-matrix heatmaps to identify the most similar document pairs
- **Bigram language model:** built a bigram probability table from a small corpus (word-pair counts → conditional probabilities), then used it to score full-sentence probabilities — including comparing a grammatical sentence against one built from unseen word pairs (probability = 0)

### Assignment 3 — Text Classification
**File:** `Assignment3.ipynb`

- **Feature engineering sweep:** systematically compared CountVectorizer vs. TfidfVectorizer, with and without stop-word removal, across unigram/bigram/trigram feature sets, observing how each choice changes the resulting feature space
- **Naive Bayes classification:** implemented the classic "Chinese/Japan" text classification example (predicting document class from word frequencies) using Multinomial Naive Bayes
- **Logistic regression evaluation:** trained logistic regression classifiers on the vectorized text and evaluated with confusion matrices, precision/recall/F1 classification reports, ROC-AUC, and log loss
- **Zipf's Law:** explored word-frequency distribution effects on model performance as part of the feature engineering comparison

## Skills demonstrated
- Core NLP preprocessing: tokenization, stopword removal, stemming
- Implementing classic NLP algorithms from scratch (edit distance, bigram language models, BoW similarity scoring)
- Vector space modeling: Count vs. TF-IDF vectorization, cosine similarity, feature space visualization
- Text classification with Naive Bayes and Logistic Regression, including full evaluation methodology (confusion matrix, ROC-AUC, log loss)
- Systematic feature engineering comparison (n-gram range, stop words, vectorizer choice)

## Tools & Technologies
Python, NLTK, spaCy, scikit-learn (CountVectorizer, TfidfVectorizer, MultinomialNB, LogisticRegression), pandas, NumPy, Matplotlib, Seaborn

## Notes
These notebooks build NLP concepts from first principles (e.g., implementing edit distance and bigram probability calculations manually) before applying library-based tools — reflecting an emphasis on understanding the mechanics behind common text-mining techniques, not just calling a function.
