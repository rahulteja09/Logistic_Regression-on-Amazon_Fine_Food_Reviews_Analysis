# Logistic_Regression-on-Amazon_Fine_Food_Reviews_Analysis
Given a review, Using Logistic Regression model determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2). [Q] How to determine if a review is positive or negative? 
[Ans] We could use Score/Rating. A rating of 4 or 5 can be cosnidered as a positive review. A rating of 1 or 2 can be considered as negative one. A review of rating 3 is considered nuetral and such reviews are ignored from our analysis. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

Models used: Sklearn LogisticRegression, Vectorizers used : Bow (sklearn-CountVectorizer),Tfidf(sklearn-TfidfVectorizer),Avg-W2v(trained a gensim model), Tfidf-W2v ,Metrics used: auc(sklearn's roc_auc) and Accurcy

Obtained results
+------------+---------+----------+----------------+------+
| Vectorizer | penalty | Accuracy | Hyperparameter | AUC  |
+------------+---------+----------+----------------+------+
|    Bow     |    l2   |  92.424  |     0.001      | 0.9  |
|    Bow     |    l1   |  92.472  |      0.1       | 0.87 |
|   Tfidf    |    l2   |  93.614  |     0.001      | 0.9  |
|   Tfidf    |    l1   |  94.239  |      0.01      | 0.93 |
|  Avg-W2v   |    l2   |  89.005  |       1        | 0.83 |
|  Avg-W2v   |    l1   |  89.008  |       1        | 0.83 |
| Tfidf-W2v  |    l2   |  87.789  |      0.1       | 0.81 |
| Tfidf-W2v  |    l1   |  87.789  |       1        | 0.81 |
+------------+---------+----------+----------------+------+
