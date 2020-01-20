# How to make MOST of your let accommendations - Are there easy ways to INCREASE your review scores rating?

## Introduction

AirBNB is obviously a great way to make some extra money if you own some unused space in a popular city. However, how can you optimize this since you compete with many other accommendations. What would people select for a stay if there a different options fulfilling their requirements in terms of location, amenities, size and similar features? Yes, the price is probably in important thing. But here it definitly depends on the peoples overall budget for what they are looking. In the end, the review scores rating by other visitors might play an important role.

Is there a way to predict the actual scores rating from the features of an accommendation? If so, could you increase your scores rating by adding a few additional amenities to your accommendation? Let´s take a look into some data to get an answer: In my analysis, I used Boston AirBNB data downloaded from Kaggle. The data is available [here](https://www.kaggle.com/airbnb/boston/data) (select the file "listings.csv"). It consits of data from 3585 accommendations in Boston.

## Business questions

Although there is one main question described above, there are a number of additional questions which help to answer how to increase your score rating.

* Question 1: Is there a relation between price an review score rating, e.g. for low and high prices?
* Question 2: Are there differences in review scores rating and price between different neighbourhoods? This is something you cannot influence if you have a given accommendation for let.
* Question 3: Is there a relation between number of reviews and review scores rating?
* Question 4: Is there a relation between amenities and review scores rating? Which amenties seems to be the most important ones?
* Final questions 5: Is there a way to predict the review score ratings based on the other information from the dataset?

## Data preparation

Before starting the analysis, it was necassary to prepare the data. For example, the price column contained $-signs and commas as decimal seperators. The amentites of the different accommendations have been encoded as combined strings in one column of the dataset. Furthermore, there are several categorial varibales e.g. for neighbourhood and type of the property. These columns has been replaced by binary dummy columns in order to allow the creation of linear regression models.

## Question 1: Is there a relation between price an review score rating?
## Question 2: Are there differences in review scores rating and price between different neighbourhoods?
## Question 3: Is there a relation between number of reviews and review scores rating?
## Question 4: Is there a relation between amenities and review scores rating?
## Final questions 5: Is there a way to predict the review score ratings based on the other information from the dataset?

## Conclusion

The results shows that there seems to be no way to predict the reviews scores rating from the information of an accommendation in the dataset. This might be disappointing to owners of unused space in the big attractive cities on this plant. However, one possible explanation might also be a bit soothing.

The reason to give a high or a low rating might base on the overall experience of a stay. It is not about price or amentities, since here people can have completly different demands. In the end, it might be e.g about support of the renters in case of issues or about cleanliness.

If you want to see some more details, see my Jupyter notebook I have created for this analysis in my GitHub repository [here](https://github.com/MiRoDS/DataScience_Project1).
