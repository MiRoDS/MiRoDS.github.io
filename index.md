# How to make MOST of your let accommendations - Are there easy ways to INCREASE your review scores rating?

## Introduction
AirBNB is obviously a great way to make some extra money if you own some unused space in a popular city. However, how can you optimize this since you compete with many other accommendations. What would people select for a stay if there are different options fulfilling their requirements in terms of location, amenities, size, and similar features? Yes, the price is probably an important thing. But this definitly depends also on the peoples overall budget they want to spend. In the end, the review scores rating by other visitors might play an important role.

Is there a way to predict the actual scores rating from the features of an accommendation? If so, could you increase your scores rating by adding a few additional amenities to your accommendation? Let´s take a look into some data to get an answer: In my analysis, I used Boston AirBNB data downloaded from Kaggle. The data is available [here](https://www.kaggle.com/airbnb/boston/data) (select the file "listings.csv"). It consists of data from 3585 accommendations in Boston.

## Business questions
Although there is one main question described above, there are a number of additional questions which help to answer how to increase your score rating.

* Question 1: Is there a relation between price and review scores rating, e.g. for low and high prices?
* Question 2: Are there differences in review scores rating and price between different neighbourhoods? This is something you cannot influence if you have a given accommendation for let.
* Question 3: Is there a relation between number of reviews and review scores rating?
* Question 4: Is there a relation between amenities and review scores rating? Which amenties seems to be the most important ones?
* Final questions 5: Is there a way to predict the review scores rating based on the other information from the dataset?

Note: Although I focused on the price per night and the overall review scores rating. There are some specific columns in the dataset like weekly price or the rating for cleaniness, but these are not taken into account here. 

## Data understanding and preparation
Before starting the analysis, it was necassary to prepare the data. For example, the price column contained $-signs and commas as decimal seperators. The amenities of the different accommendations have been encoded as combined strings in one column of the dataset. Furthermore, there are several categorial varibales e.g. for neighbourhood and type of the property. These columns have been replaced by binary dummy columns in order to allow the creation of linear regression models. Finally, rows with missing values in the review scores rating column have been removed which reduces the number of rows to 2772.

The following histograms show the distributions of the price and the review scores rating. It is noticeable that the distribution of the rating is strongly left-skewed and that nearly a fifth of the accommendation has the highest possible rating.

![Histogram: Distribution of the price (per night)](./images/price_hist.png "Distribution of the price (per night)")

![Histogram: Distribution of the review scores rating](./images/review_scores_rating_hist.png "Distribution of the review scores rating")

Furthermore, the distribution of amenties over all accommendations has been caluculated. It is shown in the following plot.

![Histogram: Distribution of amenities](./images/amenities_hist.png "Distribution of amenities")

## Question 1: Is there a relation between price and review scores rating?
The price might be an important factor for the the review scores rating. Maybe a cheap price indicates a higher probability that the stay is in the end not as pleasant as expected? Or maybe people renting an accommendation with a high price have higher demansds and would not tolerate any shortcomings which would result in a lower rating. However, the following scatter plot shows the relation between the two measures:

![Scatterplot: Relation between price and review scores rating](./images/question1.png "Relation between price and review scores rating")

Although, it uncovers some trend, the Pearsons correlation coefficient is just at 0.106, indicating only a slight correlation. Interestingly, the variance in review scores rating is higher in lower price regions. In high price regions, there seem to be no real bad ratings. Nevertheless, the number of data points is relatively low here. Thus, as an answer, yes, there is a slight correlation.

## Question 2: Are there differences in review scores rating and price between different neighbourhoods?
It has been checked whether there are differences in review scores ratings and price between different neighbourhoods. Obviously, there are price differences between different neighbourhoods in every city. However, what if a scatterplot is used to compare the review scores rating and the price for each accommendation based on the mean values for each neighbourhood. It looks as follows:

![Scatterplot: Price against review scores rating](./images/question2.png "Price against review scores rating")

It is not looking nice but the Pearsons correlation coefficient is already 0.318. Thus, there is a dependency to the neighbourhood. Higher ratings indicates here to stay in a more expensive neighbourhood. However, this cannot be influences by the renter. Furthermore, the correlation is still weak since a lot of people might decide to stay in a specific neighborhood for specific reasons not covered here and others might be completely happy with a cheap neighbourhood.

## Question 3: Is there a relation between number of reviews and review scores rating?
Before making predictions, it is checked whether the number of reviews show some correlation with the review scores rating, especially due to the very strongly skewed distribution of review scores rating.

![Scatterplot: Number of reviews against review scores rating](./images/question3.png "Number of reviews against review scores rating")

The scatterplot shows an interesting pattern, however, the correlation coefficient not indicates a relation between the two measures (Pearson correlation coefficient: 0.023). Obviously, the individual review score rating means of accommendations with a lower number of reviews have a higher variance in comparison to accommendations with many reviews. Thus, the number of reviews is not taken into account for the further analysis.

## Question 4: Is there a relation between amenities and review scores rating?

## Final questions 5: Is there a way to predict the review scores rating based on the other information from the dataset?

## Conclusion
The results shows that there seems to be no way to predict the reviews scores rating from the information of an accommendation in the dataset. This might be disappointing to owners of unused space in the big attractive cities on this plant. However, one possible explanation might also be a bit soothing:

The reason to give a high or a low rating might base in the end on the overall experience of a stay. It is not about price or amentities, since here people can have anyway completly different demands. In the end, it might be e.g. about support of the renters in case of issues or other soft factors. This is something for which an additional analysis would be interesting. However, we cannot not learn this from the given dataset.

If you want to see some more details, see my Jupyter notebook I have created for this analysis in my GitHub repository [here](https://github.com/MiRoDS/DataScience_Project1).
