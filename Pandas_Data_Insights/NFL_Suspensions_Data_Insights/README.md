# NFL Suspensions Data Insights
The following data and description comes from FiveThirtyEight! I'm exploring their NFL suspensions dataset with pandas data manipulation and mapping techniques.

This program gets into more advanced data insights (compared to the [Alcohol Consumption Data Insights](https://github.com/Kyle-Pu/Fun-With-Python/tree/master/Pandas_Data_Insights/Alcohol_Consumption_Data_Insights)) including grouping, sorting, and multi-indexing. 

## Some Neat Functions and Algorithms
* groupby() is a neat function I used here to 
* I used multi-indexing to find team breakdowns that went from team --> player --> number of suspensions for that player
	* The data came out really neatly and easy to read for this part which surprised me

## Programs
* groupingAndSorting.py: Understanding NFL suspension data
!
## [Reference](https://github.com/fivethirtyeight/data/tree/master/nfl-suspensions)
This folder contains data behind the story [The NFL’s Uneven History Of Punishing Domestic Violence](http://fivethirtyeight.com/features/nfl-domestic-violence-policy-suspensions/).

Header | Definition
---|---------
`name` | first initial.last name
`team` | team at time of suspension
`games` | number of games suspended (one regular season = 16 games)
`category` | personal conduct, substance abuse, peformance enhancing drugs or in-game violence
`desc.` | description
`year` | year of suspension
`source` | news source
