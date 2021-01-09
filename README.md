# Bestsellers-Genre-Price-and-Rating-Influences-and-Prediction

## Files of this Repository
* the-world-belongs-to-those-who-read.ipynb
* README.md

## Libraries
The following libraries are used for the data analysis:
* numpy
* pandas
* matplotlib.pyplot
* seaborn
* re
* nltk
* wordcloud
* sklearn
* xgboost
* PIL


## The Underlying Data
This is based on a dataset on Amazon's Top 50 bestselling books from 2009 to 2019. The data has been categorized into fiction and non-fiction using Goodreads. Goodreads is an American social cataloging website that allows people to search their database of books, annotations, quotes, and reviews. 

Features: 
* Name (String): Name of the Book
* Author (String): Author of the Book
* User Rating (Float): Amazon User Rating
* Reviews (Integer): Number of reviews written on Amazon
* Price (Integer): Price of the book (as at 13/10/2020)
* Year (Integer): The Year(s) it ranked on the bestseller
* Genre (String): Whether fiction or non-fiction


## Questions to be Answered
With the data analysis the following questions will be answered and visualized:
* Which Authors Write the Most Bestsellers?
* Which Genre Dominates which Year?
* How does the Mean Price Change over Years?
* What's the Mean Price in each Genre?
* Which Books have the Most Reviews?
* Do Genres Differ in the Number of Reviews?
* Which Books have the Highest User Rating?
* How does the User Rating Change over the Years?
* Does a Higher Rating Lead to a Higher Price?
* Which Words make a Bestseller's Title?

With the models the following questions will be answered:
* What's the genre of a book? This is actually a real life use case. I recently talked to a Data Scientist working at a bookselling company. They are currently working on models to determine the genre of their books. 
* What's the worth (price) of a book? Clearly this is an important question for authors, booksellers as well as customers.
* How popular is a book? This allows authors and booksellers to find out the preferences of readers and to improve their work.

## Data Analysis
The data analysis includes some NLP techniques.

## Model
The models use GridsearchCV in a pipeline to finetune and find the best estimator.

## Results
* In order to predict the genre logistic regression is the right choice. For the price it's lasso regression and for the user rating ridge regression. This is an example that shows: XGBoost is not always the right choice. We still have to find out the best model for each specific case. 
* The models can only be used to a very limited extent. Since they were calculated on the basis of data about bestsellers, they can only be used for predictions concerning bestsellers. For example there would never be a prediction of the user rating under 3. 
* To predict the genre only for fiction and non fiction can be unsatisfactory. In reality, the genre would have to be divided in much more detail.

## Acknowledgements
You can find the Licensing for the data and other descriptive information at the Kaggle link available here:
https://www.kaggle.com/sootersaalu/amazon-top-50-bestselling-books-2009-2019
