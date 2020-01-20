# How to make MOST of your let accommendations - Are there easy ways to INCREASE your review scores rating?

## Introduction
AirBNB is obviously a great way to make some extra money if you own some unused space in a popular city. However, how can you optimize this since you compete with many other accommendations. What would people select for a stay if there are different options fulfilling their requirements in terms of location, amenities, size, and similar features? Yes, the price is probably an important thing. But this definitly depends also on the peoples overall budget they want to spend. In the end, the review scores rating by other visitors might play an important role.

Is there a way to predict the actual scores rating from the features of an accommendation? If so, could you increase your scores rating by adding a few additional amenities to your accommendation? Let´s take a look into some data to get an answer: In my analysis, I used Boston AirBNB data downloaded from Kaggle. The data is available [here](https://www.kaggle.com/airbnb/boston/data) (select the file "listings.csv"). It consists of data from 3585 accommendations in Boston.

## Business questions
Although there is one main question described above, there are a number of additional questions which help to answer how to increase your score rating.

* Question 1: Is there a relation between price an review score rating, e.g. for low and high prices?
* Question 2: Are there differences in review scores rating and price between different neighbourhoods? This is something you cannot influence if you have a given accommendation for let.
* Question 3: Is there a relation between number of reviews and review scores rating?
* Question 4: Is there a relation between amenities and review scores rating? Which amenties seems to be the most important ones?
* Final questions 5: Is there a way to predict the review score ratings based on the other information from the dataset?

## Data preparation
Before starting the analysis, it was necassary to prepare the data. For example, the price column contained $-signs and commas as decimal seperators. The amentites of the different accommendations have been encoded as combined strings in one column of the dataset. Furthermore, there are several categorial varibales e.g. for neighbourhood and type of the property. These columns have been replaced by binary dummy columns in order to allow the creation of linear regression models.

## Question 1: Is there a relation between price an review score rating?
The price might be an important factor for the the review scores rating. Maybe a cheap price indicates a higher probability that the stay is in the end not as pleasant as expected? Or maybe people renting an accommendation with a high price have higher demansds and would not tolerate any shortcomings which would result in a lower rating. However, the following scatter plot shows the relation between the two measures:
![Scatterplot](./question1/png "Scatterplot")
Although, it shows some relation, the Pearsons correlation coeficient is just at 0.106, indicating only a slight correlation. Interestingly, the variance in review scores rating is higher in lower price regions. In high price regions, there seem to be no real bad ratings. Nevertheless, the number of data points is relatively low here. Thus, as an answer, yes, there is a slight correlation.

## Question 2: Are there differences in review scores rating and price between different neighbourhoods?

## Question 3: Is there a relation between number of reviews and review scores rating?

## Question 4: Is there a relation between amenities and review scores rating?

## Final questions 5: Is there a way to predict the review score ratings based on the other information from the dataset?

## Conclusion
The results shows that there seems to be no way to predict the reviews scores rating from the information of an accommendation in the dataset. This might be disappointing to owners of unused space in the big attractive cities on this plant. However, one possible explanation might also be a bit soothing:

The reason to give a high or a low rating might base in the end on the overall experience of a stay. It is not about price or amentities, since here people can have anyway completly different demands. In the end, it might be e.g. about support of the renters in case of issues or other soft factors. This is something for which an additional analysis would be interesting. However, we cannot not learn this from the given dataset.

If you want to see some more details, see my Jupyter notebook I have created for this analysis in my GitHub repository [here](https://github.com/MiRoDS/DataScience_Project1).
