# 2019 Canadian Federal Election Result Prediction Based on Tweets
The purpose of this project is to gain insight about the 2019 Canadian federal election result from tweets using natural language processing. Also, machine learning models are trained to classify either a tweet is positive or negative.
### Dataset
The datasets analyzed in this project are Canadian_elections_2019.csv and Sentiment.csv, which contains 2700+ political topics related tweets and 130,000+ general tweets respectively. In Canadian_elections_2019.csv, each tweet is classified as either positive or negative. Some of the reasonings behind the classification results are provided. Sentiment.csv contains only the tweets and their positive/negative classification results.  
### Pre-processing
The following steps are done to analyze the datasets: 
1. Data cleaning (Remove empty entries, Remove stopwords, Remove html tags and emojis, Convert to lower case, etc.)
2. Determine the political party each tweet mentioned
3. Feature engineering with TF-IDF and WF, while excluding infrequent words
### ML Model Development
The following models are tuned through grid-search of the hyper-parameters.  
- Logistic Regression
- k-NN
- Naive Bayes
- SVM
- Decision Tree
- XG Boost
- Random Forest  

Cross validation are implemented in most of the models, but not to some due to exccesive load of calculation.  
After all models are tuned, the top 2 performing models are implemented to the tweets of each party individually.
### Negative Reason Classification
At last, ML models are tuned to classify the reason that a tweet is negative, which has 10 classes in totol. Due to the small sample size, overfitting became an issue. Penalties are assigned to prevent overfitting, but still the problem is not fix perfectly. 
### More Advanced approach
TF-IDF is a common way of NLP feature engineering, but it is not enough in many cases since it does not conserve the relationship between context. Therefore, neural nets can be a better choice. Due to the time limit of this project, NN approach is not implemented, and might be implemented in the future projects.
