# Predicting Triathlon Finish Time 

Project Partner [Adam Liscia ](https://github.com/AdamLiscia)

Looking into the effects of weather on the results of Ironman Kona, looking into why 2018 had such fast results, and to be able to predict average times based on weather.

![](/media/winner.png)

We first wanted to assess the finish times of all the athletes, but the data becomes skewed and the 17 hour cut off time starts to effect our data. That when we decided to limit our filed to just the pros who have a more normally distributed set of times.
We first wanted to try using each athlete's country as a feature, but then decided that continent was a much more meaningful feature to use instead.

# Some Cool Feature Engineering
The first 2 days of our project were spent on cleaning our data and figuring out what how we wanted to represent our data.

Some issues we ran into:

Wind direction was given as S, SSW, SW, WSW, and W. This didn't seem to be exactly categorical because there are relationships between these directions. We decided to over come this by use sin and cos to break the wind direction and speed into it's X and Y components.




# Data Exploration

![correlation with average temparature](/media/avgtemp.png)



