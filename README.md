### Using Reddit's API to Predict Number of Comments

This project was the third project of the Data Science Immersive course at General Assembly NYC, which I completed during week 5 of the course. The general purpose was to utilize two major skills: collecting data with an API and building a binary classification model. I aimed to predict which features would predict whether or not a post on reddit makes it to the "hot" subreddit, which is a page for posts with high user interaction, as measured by the number of comments on the post. To gather the data, I scraped JSON post data from reddit's API and saved it to a .csv file. I set the target variable to a binarized measure of number of comments: above the mean amount of comments or below it.

I tried a few different kinds of models. Because there was text data and numerical data, I initially isolated them to look at how they performed on their own. A Logistic Regression model on only the numerical data gave me an accuracy score of 0.88, which is just short of the score for my best model. Using Count Vectorizer on the post title and running it through a Bernoulli Naïve Bayes model, I got a score that was about the same as the baseline. Hoping that a combination of these two initial approaches would give me a higher score, I used FeatureUnion to fit two pipelines inside a pipeline in order to combine text and numerical data. This resulted in a better score (0.91), but not as much as an improvement from the baseline as I had hoped for. Moving forward I would like to try both a regression model and a multi-class classification model.


### Repository Contents

- Reddit_Predicting_Comments, the main Jupyter Notebook 
- Data folder, containing the scraped data (3 .csv files)
- An accompanying blog post can be found [here](https://confoley.github.io/Reddit_Predicting_Comments/)

### Imports Used
- Pandas
- NumPy
- Requests and JSON
- Time
- Scikit-Learn
- Matplotlib
- Seaborn
- Ast
- Itertools

Data Source: Reddit API



