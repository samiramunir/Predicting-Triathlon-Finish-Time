# Predicting Triathlon Finish Time 

Project Partner [Adam Liscia ](https://github.com/AdamLiscia)

Looking into the effects of weather on the results of Ironman Kona, looking into why 2018 had such fast results, and to be able to predict average times based on weather.

![](/media/winner.png)

We first wanted to assess the finish times of all the athletes, but the data becomes skewed and the 17 hour cut off time starts to effect our data. That when we decided to limit our filed to just the pros who have a more normally distributed set of times.
We first wanted to try using each athlete's country as a feature, but then decided that continent was a much more meaningful feature to use instead.



## Some Cool Feature Engineering from the get go 


Wind direction was given as S, SSW, SW, WSW, and W. This didn't seem to be exactly categorical because there are relationships between these directions. We decided to over come this by use sin and cos to break the wind direction and speed into it's X and Y components. We created dummy variables for male, females, continents and year




## Data Exploration

The race has three parts, swim, bike and run in order. The following graphs shows the finish times for each and also the aggregate. 

![](/media/protimes.png)

The following graphs show correlation betwen various weather parameters and overall finish times. 


![correlation with average temparature](/media/avgtemp.png)

![correlation with average temparature](/media/humidity.png)

![correlation with average temparature](/media/windspeed.png)



## Some  Cool Feature Engineering & Selection


Scaled data using Standardscaler from sklearn preprocessing. 
Raised the degree of the equation to the second degree resulting in 350 features from the initial 25. We then using the VariancThreshhold module from sklearn to removes all low-variance features and ended up with 26 features. 

We then looked  at the correlation matrix of these features and dropped the highly correlated ones. Resulting in 17 final number of features. 



![correlation with average temparature](/media/autocorrelation.png)

After doing another set of feature selection using sklearn's SelectKBest. We used an OLS regression model to fit the data. The scores are as follows. 
![correlation with average temparature](/media/OLSregression.png)



Since our or R^2 is .463, we need more data to produce a more accurate model.






