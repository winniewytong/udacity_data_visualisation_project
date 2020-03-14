
# Bay Wheels Data Exploration

## Dataset

The data from Lyft/ Bay Wheels consists of information regarding 296,000 bike rental information in January 2020 including duration, pick-up and drop-off location, user type, pick-up and drop-off time, and other additional user information. The dataset can be found on Lyft's website [here](https://www.lyft.com/bikes/bay-wheels/system-data),
the file called **202001-baywheels-tripdata.csv.zip** can be found under this folder [here](https://s3.amazonaws.com/baywheels-data/index.html).


## Summary of Findings

In the exploration, I found that there was a strong relationship between the number of rentals and the start hour of the bike hire. The number of rentals increases during morning and late afternoon (i.e. office hours). The relationship became obvious once the duration period is transformed to minutes instead of seconds. The duration of rental started climbing up during office hours as well. After transforming the duration period (min) to a logarithmic scale, I found that most bikes were rented for about 10 minutes. In my analysis I found that location of the drop-off depot had a positive effect on the duration of rental: users who returned the bike at the same depot had a longer rental duration. This effect became more obvious and a trend could be observed when an additional categorical variable *week day* was added in the analysis: the average duration of rental for users who returned bike at the same depot was consistently longer throughtout the week. 

When looking at the general statistics of user type in my initial univariate exploration, I couldn't find anything particularly interesting. However, once I used a point plot to analyse the average duration by week day and user type, an interesting user behavioural trend could be brought to light - casual customers hired bikes for a longer time on average on Friday and Saturday. 

Outside of the main variables of interest, I analysed a group of users who constantly rented bikes for about 66 minutes at different hours thoroughout the day using different dimensions. However, due to a lack of customer information (such as customer id), it was hard to draw any conclusions to explain the behaviour of this odd group of users. 


## Key Insights for Presentation

For the presentation, I focus on factors contributing to the duration of bike rentals. I start by introducing the
duration (min) variable, followed by other categorical variables using histograms, barcharts and piecharts. 

After introducing different variables, I use scatterplot, boxplot, violinplot and pointplot to explore relationships between duration of bike hire and start hour, week day, user type and return location. I use different colours and type of graphs to demonstrate relationships and to avoid confusions. 

