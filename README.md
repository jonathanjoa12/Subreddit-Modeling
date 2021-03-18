# Project 3 - NLP


### Overview

The stock market has gained significant popularity since the COVID-19 pandemic started. This means that thousands of brokerage accounts opened. There are two ways to trade in the stock market. One is trading regular shares itself. Another way is trading options. These two ways of trading are different to each other. Much of these users rely on news and posts in attempt to optimize their profits and experience in the stock market. One way is by reading the news on a daily basis. Another way is to get opinions from other traders or analysts through platforms like reddit. This project seeks to analyze the two subreddits of stock market and options and differentiating them by the posts of users. Through the posts of users, we can use the text to create a model.


### Problem Statement:
     
The goal os this project will be to analyze some recent subreddit posts among various stocks and to analyze whether a post is is regards to the stock market or the options subreddits, making it a binary classification problem. The importance of this is to distinguish between the general stock market and options. Options is an important subsection of the stock market which increases the complexity and difficulty of this model. Success of the model will be evaluated through classification metrics inclduing accuracy, precision, etc.
The primary audience of this model includes but is not limited to: first-time stock market investors and those interested in economics or security analysis. 

### Brief Summary of the Process

The first step before modeling is preprocessing which involves extracting the textual data from a portion of the amount of posts on the subreddit pages. We have to extract the data using API or Application Programming Interface. By using the Python Reddit API Wrapper (PRAW). We extracted approximately 1000 posts per subreddit page with the wrapper. From the generator, a single dataset was created with webscrapping that involved posts from both models. After the single dataset was created, there exploratory data analysis conducted to make sure there were no null values.The X variable includes the text data from our merged subreddits. The Y variable includes the specific subreddit that the text came from. Before setting the response variable, the subreddits have to be mapped from stock market and options to 1 and 0 respectively. Since the model is trying to classify between two different subreddits, the most ideal type of model that would be used to represent this data is a Naive-Bayes regression model. A CountVectorizer was instantiated to convert the text data to numerical data. Afterwards, the CountVectorizer helped generate the highest word usage throughout the text data. The first bar graph shown represents the highest amount of words within the text. However, almost all of the words included stop words within the English language which meant that the data had little to no meaning to it. Therefore, the exploration of stop word removal was implemented and more descriptive words were represented in the second bar graph that had meaning with respect to the subreddit posts.The second model implemented was the Random Forest Classifer through a gridsearch fit to find the best scores through the best parameters. After fitting the X and Y variables, scores and classification metrics were generated for analysis.
     
### Results and Analysis
    
The scores and classification metrics were as follows:
RandomForest and Naive-Bayes Regression models scored almost the same in sensititivty, precision, and specificity. However, there is a noticable difference when it came to accuracy. The accuracy score on the original model is about 80% while the accuracy score on the random forest model is seven points higher with a score of 87%. This shows that the random forest model provides a better insight in classifying the two different subreddits. 
From our classification metrics, we see that specificity has the highest rate. 
The best classification metrics that would be used for classifying subreddits would involve precision and sensitivity because you would want to make a case for minimizing false positives and false negatives for precision and sensitivity respectively. The reason for these two metrics being selected is because often on reddit, you are making use of their search engine and want to get search results that produce the best results as possible.
 

### Recommendations/Downsides of Models
   
The model overall performed better than expected considering the topics of the two subreddits chosen were signficantly similar to each other. However, through exploration of two different classification models, the random forest model performed better than the original Naive-Bayes regression model. After one analyzes the models, they may have a better idea of which subreddit the post came from. However, there would be improvements to the model because while running the model, the computational time was longer than expected. This occurred throughout the fitting part of the model because the amount of text to process was big. Therefore, that is one aspect of improvement that can be implemented.
     
      



