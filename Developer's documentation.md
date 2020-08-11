## Introduction
In this course project, I applyied machine learning algorithms to predict the final price of each residential home in Ames, Iowa, using 79 explanatory variables describing most aspects of these homes. The end-user of this project could be someone who plans to buy a house in Ames or real estate agents. A minimum viable product (MVP) out of this project could be a Jupyter notebook that users can use to predict the sale price of houses in Ames after entering the required information. This project is based on supervised machine learning (ML) algorithms. I built an ML model using the existing data (i.e., the known sale price of Ames houses with different aspects) and then use this model to predict the sale price of a specific house after users enter the required information. The dataset was originally prepared by Dean De Cock and was slightly revised by Kaggle https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data As an MVP, the GUI of this product might be just a Jupyter notebook. But if possible, I might make it more user-friendly.

Since I use Jupyter Notebook for this project, I have added detailed in-code documentation there. In this document, I would like to share some of my major considerations.

## Missing data
I have been working on handling missing data until later on this project. However, after realizing I might not need these many variables in my final model. My data exploration has shown that most variables with huge amount of missing values are not very relevant in predicting the final sale price of a house. Hence, I didn't deal with missing values in predicting.ipynb.

## Feaure engineering
Needless to say, square footage is important when selling a house. Hence I added a new feature called TotalSF.

``` 
train_test['TotalSF'] = train_test['TotalBsmtSF'] + train_test['1stFlrSF'] + train_test['2ndFlrSF']
```

## Tradeoff between a more accurate model and user’s burden in entering too much information
The dataset has 79 features but several of features have an extremely high percentage of missing values. Some features seem to be only remotely related to the target. Hence, I decided to figure out the feature importance after hearing my instructor's feedback. At first, I was trying to use a fancier way (permutation feature importance) using the package eli5. But I run into a serious error when I was trying to split my dataset into training and testing sets. After a painful debugging, I solved the issue and the error is not related to eli5. However, I found out permutation importance seems to be not very helpful in my case because the importance values for many features are almost the same. Eventually, I went back to the simpler solution, using the built-in function in random forest algorithm in scikit-learn. I chose the top 20 most important features to build the final predicting model.

## Separating the notebook I used to explore the data (and build the ML model) and the notebook for end users to make predictions
At first, I thought only one Jupyter notebook would be enough but I soon realzied that end users might not need to see the whole thing about data exploration, data cleaning, feature selection, and final model building. What users expect is simply a workable predicting model that can make relatively accurate predictions. Too much code might make users feel overwhelmed. 

## Thoughts about coding
In this project, I did not use very fancy coding concepts. Thanks to the powerful pacakges (e.g., pandas and scikit-learn) in data science, most functions I need to clean the data and conduct the machinie learning models are ready to use. However, I did learn from other users on how to identify variables with missing data and on how to visualize them. Besides, I also learned how to show correlation matrix in a fancy way. Finally, I did give some thoughts on how to deal with some variables with missing values. These efforts are beyound the coding itself and require a deep understanding of the data itself.

## Known issue:
The main issue is still about user experiences. Basically, users only need to do four things: 1) install jupyter notebook, python, and python packages, 2) download files in my github folder and put them into the right place in their own folder, 3) enter information about the house of interest, and 4) run the predicting model in the Jupyter notebook.
I have not recruited any potential users to do some testing, but I suspect that step 4 would be the easiest part and users might have issues in all the other three parts. If possible, it would be better if users can get detailed guidance in each step. Screenshots could be very helpful.

## Future work
Ideally, the end product of this project would be an interactive web/app application where users enter information about a house and the web/app makes predictions and shows the results to the user. I hope I will be able to transform my current project into a full blown web/app application in the near future.

## Ongoing deployment
The current project uses historical data about the sold prices of houses in Ames. It does not involves infomation of any newly sold houses. Hence, it is not an ongoing project. 
However, it has the potential to be ongoing if the developer can continuously add information of newly sold house in the databas.
