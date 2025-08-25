# 📘 Sentiment Classification of Amazon Kindle Store Reviews
📌 Project Overview:
This project focuses on sentiment classification of Amazon Kindle Store reviews by applying text preprocessing, feature extraction, and machine learning models. The dataset contains nearly 1 million reviews, which were cleaned and transformed into numerical representations to train classification models that predict sentiment (positive/negative).



# About Dataset
Context:
A small subset of dataset of product reviews from Amazon Kindle Store category.

Content:
5-core dataset of product reviews from Amazon Kindle Store category from May 1996 - July 2014. Contains total of 982619 entries. Each reviewer has at least 5 reviews and each product has at least 5 reviews in this dataset.

Columns:
asin - ID of the product, like B000FA64PK
helpful - helpfulness rating of the review - example: 2/3.
overall - rating of the product.
reviewText - text of the review (heading).
reviewTime - time of the review (raw).
reviewerID - ID of the reviewer, like A3SPTOKDG7WBLN
reviewerName - name of the reviewer.
summary - summary of the review (description).
unixReviewTime - unix timestamp.

Acknowledgements:
This dataset is taken from Amazon product data, Julian McAuley, UCSD website. http://jmcauley.ucsd.edu/data/amazon/

License to the data files belong to them.


Inspiration:
Sentiment analysis on reviews.
Understanding how people rate usefulness of a review/ What factors influence helpfulness of a review.
Fake reviews/ outliers.
best rated product IDs, or similarity between products based on reviews alone (not the best idea ikr).
Any other interesting analysis.

# 🔄 Preprocessing & Cleaning

1. Lowercasing all text
2. Removing punctuation, URLs, and HTML tags
3. Removing extra whitespaces
4. Removing stopwords
5. Lemmatization to normalize words


# 🔑 Feature Engineering
1. Bag of Words (BoW)
2. TF-IDF Vectorizer
3. Word2Vec embeddings (100 dimensions, averaged per review)

# 🤖 Models Applied
1. Multinomial Naive Bayes
2. Logistic Regression
3. Random Forest Classifier


# 📊 Results:
1. 

<img width="906" height="676" alt="Screenshot 2025-08-25 225745" src="https://github.com/user-attachments/assets/5937b090-a132-46d6-b684-7c8a26399884" />

2. 
<img width="882" height="663" alt="Screenshot 2025-08-25 225808" src="https://github.com/user-attachments/assets/ae6eaaf4-b5bc-43dc-86b6-ac57461c38ed" />

3. 

<img width="872" height="735" alt="Screenshot 2025-08-25 225829" src="https://github.com/user-attachments/assets/90c6a7cb-10b7-4117-b4ac-091173baca22" />


# 💾 Model Deployment Readiness

Trained models saved in .pkl format using pickle
Ready for integration into a Flask/Django app or any ML pipeline

# 🚀 How to Run

1. Clone this repository
2. Install dependencies: pip install -r requirements.txt
3. Run preprocessing and training script
4. Saved models (.pkl) and processed dataset (df_up.csv) will be available for reuse.


# 📌 Key Learnings

1. Handling large-scale text data efficiently
2. Comparing feature extraction methods for NLP
3. Model evaluation with imbalanced data
4. Building deployment-ready ML models





