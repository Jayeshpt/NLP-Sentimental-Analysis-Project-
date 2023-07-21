# Sentiment Analysis on Musical Instruments Reviews
This project aims to perform sentiment analysis on a dataset containing musical instruments reviews. The goal is to predict whether a review is positive, negative, or neutral based on the overall rating given by the reviewer.

### Dataset
The dataset used in this project is stored in a CSV file named Musical_instruments_reviews.csv. It contains the following columns:

### reviews: Textual content of the reviews.
### sentiment: The target column containing the sentiment label (positive, negative, or neutral).
### Data Preprocessing
Removed unwanted features: The original dataset had several columns that were not necessary for sentiment analysis. I dropped columns such as reviewerID, asin, reviewerName, unixReviewTime, helpful, and reviewTime.

Handling missing values: There were 7 missing values in the reviewText column. To handle them, I filled the missing values with "Missing".

Concatenating review text and summary: I combined the reviewText and summary columns into a single column named reviews.

Creating the sentiment column: Based on the overall rating, I assigned labels to each review. If the rating is greater than 3, the sentiment is positive. If it is less than 3, the sentiment is negative. If the rating is exactly 3, the sentiment is neutral.

### Data Cleaning
The review text was cleaned using the following steps:

* Make text lowercase.
* Remove text in square brackets.
* Remove links.
* Remove punctuation.
* Remove words containing numbers.
* Tokenization and Lemmatization.
* Removal of stopwords.

### Model Building and Evaluation
I used four different classifiers to build the sentiment analysis models: Naive Bayes, Random Forest, Linear SVM, and Logistic Regression. The models were trained using both the Bag-of-Words (BoW) and Term Frequency-Inverse Document Frequency (TF-IDF) approaches.

The models were evaluated using accuracy scores on a test set. Here are the accuracy results for each model:

* Naive Bayes (BoW): 88.94%
* Naive Bayes (TF-IDF): 88.89%
* Random Forest (BoW): 88.89%
* Random Forest (TF-IDF): 88.89%
* Linear SVM (BoW): 88.85%
* Linear SVM (TF-IDF): 88.99%
* Logistic Regression (BoW): 89.04%
* Logistic Regression (TF-IDF): 88.89%
* The logistic regression model with BoW achieved the highest accuracy of 89.04%.

### Prediction
I also provided a prediction example using some sample review texts to demonstrate how the models can predict the sentiment of new reviews.

Note: Please customize the README file content according to your specific project details and information. It should include essential information about the project, dataset, preprocessing steps, model building, evaluation results, and any other relevant details.
