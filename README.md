
Description:

This dataset contains prices for listing in different neighborhood groups within different neighborhood cities. It also contains different factors like property types, reviews, and availability of listings, that can affect the price for the listing. The data has 102588  observations and 18 columns. 
Response variable: Price per night
Explanatory variables: price, name, host id, host name, Neighborhood-group, neighborhood,  room-type, minimum-nights, number of reviews, last review, review per month and availability 365 days.
![image](https://user-images.githubusercontent.com/113064930/209486537-00581969-6319-4ee3-967c-935847eda9f9.png)

Problem Statement - One of the biggest challenges for companies is to maintain positive customer experience along with having a financially profitable business model for property owners. How factors are affecting the price for the Airbnb listing in NYC? What is the overall location distribution of Airbnb NYC? Which neighborhood has a better average price for the Airbnb listing?
After loading the dataset in and from the head of Airbnb open dataset I can see a number of things. These 18 columns provide a very rich amount of information for deep data exploration. I already see some missing values, which will require cleaning and handling of NaN or 0 values.
My goal is to build a statistical model to effectively predict the price for the listings and company can use this model to come up with a price suggestion for the future listings.
My Business question is - Should there be a cap on how many days a host can rent out their unit on concern that short-term rentals will erode the existing housing stock?

I identified several NaN values or missing  after looking at the head of the dataset, thus I did further investigate missing values before moving on to the analysis.
In this instance, I observed missing data does not require a lot of extra consideration. Further observations may be made based on the characteristics of our dataset: the columns "name" and "host name" are unimportant and unrelated to our data analysis, while the columns "last review" and "review per month" require fairly straight forward processing. To clarify, the term "last review" refers to the date; if there are no reviews for the listing, the term date will be absent. Since this column is unnecessary and unimportant in our situation, it is not necessary to append those data. I can see that the "number of review" field will contain a 0; consequently, following this reasoning, with 0 total reviews there will be 0.0 rate of reviews per month. For the "review per month" column, we can simply add it with 0.0 for missing data. Consequently, let’s continue with the handling of missing data and deleting unnecessary columns.

The libraries I will be using:  Rstudio, Rmarkdown

Licensing, Authors, Acknowledgements:

Data used are provided through Kaggle by NYC AirBnB : https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data
