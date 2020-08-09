# Overview of the project
This project applys supervised machine learning (SML) algorithms to predict the final price of each residential home in Ames, Iowa, using 23 explanatory variables describing most aspects of these homes. The end-user of this project could be someone who plans to buy a house in Ames or real estate agents. Jupyter notebooks were used to predict the sale price of houses in Ames after entering the required information. I built an SML model using the existing data (i.e., the known sale price of Ames houses with different aspects) and use this model to predict the sale price of a specific house after users enter the required information. The dataset was originally prepared by Dean De Cock and was slightly revised by Kaggle https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data 
For now, the project is in just a Jupyter notebook. But in the future, I might make it more user-friendly.
Below is a brief introduction of files in the folder. Files that users are involved are bolded.
1) training.ipynb: The Jupyter notebook that I used to explore the data and build the SML model.
2) **predicting.ipynb**: Based on the knowledge gained from exploring and building the model, this simplified Jupyter is for end users to make predictions.
3) ames.csv: This is the original dataset with all 79 features.
4) ames_core.csv: This is the dataset with only important features.
5) label.csv: This the documented sale price for Ames houses.
6) **user.csv**: To predic the sale price of a house in Ames, the user needs to enter the required information in each column.
7) **ReadMe.md**: This is the user's guide, the file you're reading.
8) **data_description.txt**: Users need to refer to this document when entering information.
9) Developer's documentation.md: This file documents my major considerations while working on this project.

# Requirements
Below is the version number of Python and main packages used in this project. I expect the notebook should still work with newer versions.  
- python: 3.6.5.final.0
- OS: Windows
- OS-release: 10
- pandas: 0.23.0
- numpy: 1.14.3
- scipy: 1.1.0
- IPython: 6.4.0
- matplotlib: 2.2.2

# Installation 
Before using the predicting model in this project, the user needs to make sure the following were installed (Anaconda is strongly recommended).
- Jupyter notebook
- Python 3.6.5 or later
- Python Packages: pandas, numpy, scipy, IPython, matplotlib

# Usage
The predicting model is very easy to use.
1) Make sure you have read ReadMe (this file).
2) Download everything in this folder and put them in the root folder where you can find your .ipython and .jupyter folder.
3) Open user.csv file and fill out the information required
4) Start your Jupyter notebook and double click "predicting.ipynb" to open it.
5) After opening "predicting.ipynb", click **Kernel**, and then click "**Restart & Run All**".
6) Scroll down the notebook and find out the predicting price for the house of interest.

# Known issues
No known issues for now, but I will really aprreciate it if you could let me know if issues are found out.

# Acknowledgments
I would like to thank Dr. Chris Harding for his support and guidance while I was conducting this course project.
