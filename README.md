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

-------------------BOW---------------------Multinomial Naive Bayes---------------------------
Training accuracy:0.9415968758311125
Testing accuracy:0.941560318332621
confusion matrix:[[  8295   5858]
 [  8498 223004]]
classification report:              precision    recall  f1-score   support

           0       0.49      0.59      0.54     14153
           1       0.97      0.96      0.97    231502

    accuracy                           0.94    245655
   macro avg       0.73      0.77      0.75    245655
weighted avg       0.95      0.94      0.94    245655

-------------------tfidf-------------------Multinomial Naive Bayes---------------------------
Training accuracy:0.9414706824213938
Testing accuracy:0.9422238505220737
confusion matrix:[[    44  14109]
 [    84 231418]]
classification report :              precision    recall  f1-score   support

           0       0.34      0.00      0.01     14153
           1       0.94      1.00      0.97    231502

    accuracy                           0.94    245655
   macro avg       0.64      0.50      0.49    245655
weighted avg       0.91      0.94      0.91    245655



2. 
<img width="882" height="663" alt="Screenshot 2025-08-25 225808" src="https://github.com/user-attachments/assets/ae6eaaf4-b5bc-43dc-86b6-ac57461c38ed" />

-------------------BOW---------------------logistic regression---------------------------
Training accuracy:0.9637499253694889
Testing accuracy:0.9574810201298569
confusion matrix:[[  6580   7573]
 [  2872 228630]]
classification report:              precision    recall  f1-score   support

           0       0.70      0.46      0.56     14153
           1       0.97      0.99      0.98    231502

    accuracy                           0.96    245655
   macro avg       0.83      0.73      0.77    245655
weighted avg       0.95      0.96      0.95    245655

-------------------tfidf-------------------logistic regression---------------------------
Training accuracy:0.9605340287992358
Testing accuracy:0.958783660010991
confusion matrix:[[  6261   7892]
 [  2233 229269]]
classification report :              precision    recall  f1-score   support

           0       0.74      0.44      0.55     14153
           1       0.97      0.99      0.98    231502

    accuracy                           0.96    245655
   macro avg       0.85      0.72      0.77    245655
weighted avg       0.95      0.96      0.95    245655


<img width="872" height="735" alt="Screenshot 2025-08-25 225829" src="https://github.com/user-attachments/assets/90c6a7cb-10b7-4117-b4ac-091173baca22" />


3. -----------------word2vec---------------Random forest-------------------------
Training accuracy: 0.9999767385397328
Testing accuracy:0.9480131349521348
Confusion matrix: [[  2443  14766]
 [   559 277018]]
 classification report:               precision    recall  f1-score   support

           0       0.81      0.14      0.24     17209
           1       0.95      1.00      0.97    277577

    accuracy                           0.95    294786
   macro avg       0.88      0.57      0.61    294786
weighted avg       0.94      0.95      0.93    294786



4. -----------------word2vec---------------logistic regression -------------------------

Training accuracy: 0.9503120670278977
Testing accuracy:0.9502995393268338
Confusion matrix: [[  5416  11793]
 [  2858 274719]]
 classification report:               precision    recall  f1-score   support

           0       0.65      0.31      0.43     17209
           1       0.96      0.99      0.97    277577

    accuracy                           0.95    294786
   macro avg       0.81      0.65      0.70    294786
weighted avg       0.94      0.95      0.94    294786



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




