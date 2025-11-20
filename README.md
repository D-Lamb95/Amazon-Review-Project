# Amazon Review Text Mining & Sentiment Analysis

## Overview  
This project analyzes Amazon product reviews using natural language processing (NLP) to understand customer sentiment and highlight common themes in feedback. The focus is on turning unstructured review text into structured insights through text cleaning, feature extraction, sentiment scoring, and classification.

The workflow demonstrates how organizations can use customer reviews to identify pain points, strengths, and opportunities for product or service improvement.

---

## Data Description  
The dataset consists of Amazon product reviews with fields such as:

- **reviewText** – the full text of the customer review  
- **overall** – numeric rating (e.g., 1–5 stars)  
- **summary** – short review headline  
- **reviewTime / unixReviewTime** – timestamp of the review  
- **productId / userId** – identifiers for products and users (if included)

For modeling, ratings are often mapped to sentiment labels, for example:

- 1–2 stars → negative  
- 3 stars → neutral (optional)  
- 4–5 stars → positive  

---

## Methods  

### 1. Text Cleaning  
Review text is prepared for analysis using standard NLP preprocessing steps, such as:

- Lowercasing  
- Removing punctuation and special characters  
- Tokenization  
- Stopword removal  
- Optional lemmatization or stemming  

These steps reduce noise and make the text more consistent for modeling.

### 2. Feature Extraction  
Cleaned text is transformed into numeric features using methods such as:

- Bag-of-words representation  
- TF–IDF (term frequency–inverse document frequency)

These features form the input to classification models.

### 3. Sentiment Labeling  
Sentiment labels are created using either:

- Star ratings (e.g., mapping 1–2 to negative and 4–5 to positive), or  
- A rule-based sentiment tool as a reference

This produces a target variable for supervised learning.

### 4. Modeling  
One or more classification models are trained to predict sentiment from review text features, for example:

- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)

Models are evaluated using metrics such as accuracy, precision, recall, and F1-score.

### 5. Exploratory Text Analysis  
Additional analysis can include:

- Most frequent words or n-grams in positive vs. negative reviews  
- Common themes or topics using simple keyword analysis or topic modeling  
- Distribution of ratings over time

---

## Key Insights  

- Text-based features provide a strong signal for distinguishing positive and negative reviews.  
- Frequently occurring phrases in negative reviews can indicate specific product issues or pain points.  
- Positive reviews often cluster around themes like quality, value, and reliability, while negative reviews highlight defects, poor service, or misleading descriptions.  
- The workflow can be reused for other sources of free-text feedback such as surveys, app reviews, or internal comments.

---

## Requirements  

To run the notebook or scripts, you will need:

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- nltk or spaCy (for text preprocessing)  
- jupyter (optional, for running the notebook)

Install dependencies, for example:

```bash
pip install pandas numpy scikit-learn nltk
