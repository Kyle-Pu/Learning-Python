# Modeling With Imperfect Data
Here, I explore creating machine learning models with __*missing data*__! We'll take a look at how substance abuse of various drugs and age range affect the median number of times a user in an age group used alcohol in the past 12 months.

## Handling Missing Data
We have a few different options for handling missing data:
  1. Dropping columns with missing data
  2. Using __**imputation**__ to fill in missing values with related data such as the mean, median, or mode of the numbers in the column or a specified constant.
  3. Using imputation as well as creating columns to denote whether or not the original data had a missing value in each row (True or False).

## Manual Preprocessing
__Note:__ I manually changed the age column data in the CSV file to get rid of hyphens and the plus (in "65+"). I replaced all age ranges with the average of the low and high end and replaced "65+" with 65.

## Avoiding Data Leakage
I used the imputer separately on both training and validation data instead of using the imputer to fill in missing values on the original data all at once in order to avoid data leakage. If we use the same imputer on the whole dataset at once, we risk the chance of achieving unrealistically high validation scores because the validation data was processed the same exact way as our training data. This error is called __Train-Test Contamination__, but can be avoided by imputing missing values separately on the traiing and testing/validation data!

## Type of Imputation
When I used just imputation to handle the missing values, using the most frequent value of each column to fill in missing data worked the best (gave the lowest Mean Absolute Error). There was little to no variation with imputation methods when imputing and creating tracking columns to see which rows had missing values, though (so I just used the median).

## [Reference](https://github.com/fivethirtyeight/data/tree/master/drug-use-by-age) For Data and Description Below
Source: [National Survey on Drug Use and Health from the Substance Abuse and Mental Health Data Archive](http://www.icpsr.umich.edu/icpsrweb/content/SAMHDA/index.html).

Header | Definition
---|---------
`alcohol-use` | Percentage of those in an age group who used alcohol in the past 12 months
`alcohol-frequency` | Median number of times a user in an age group used alcohol in the past 12 months
`marijuana-use` | Percentage of those in an age group who used marijuana in the past 12 months
`marijuana-frequency` | Median number of times a user in an age group used marijuana in the past 12 months
`cocaine-use` | Percentage of those in an age group who used cocaine in the past 12 months
`cocaine-frequency` | Median number of times a user in an age group used cocaine in the past 12 months
`crack-use` | Percentage of those in an age group who used crack in the past 12 months
`crack-frequency` | Median number of times a user in an age group used crack in the past 12 months
`heroin-use` | Percentage of those in an age group who used heroin in the past 12 months
`heroin-frequency` | Median number of times a user in an age group used heroin in the past 12 months
`hallucinogen-use` | Percentage of those in an age group who used hallucinogens in the past 12 months
`hallucinogen-frequency` | Median number of times a user in an age group used hallucinogens in the past 12 months
`inhalant-use` | Percentage of those in an age group who used inhalants in the past 12 months
`inhalant-frequency` | Median number of times a user in an age group used inhalants in the past 12 months
`pain-releiver-use` | Percentage of those in an age group who used pain relievers in the past 12 months
`pain-releiver-frequency` | Median number of times a user in an age group used pain relievers in the past 12 months
`oxycontin-use` | Percentage of those in an age group who used oxycontin in the past 12 months
`oxycontin-frequency` | Median number of times a user in an age group used oxycontin in the past 12 months
`tranquilizer-use` | Percentage of those in an age group who used tranquilizer in the past 12 months
`tranquilizer-frequency` | Median number of times a user in an age group used tranquilizer in the past 12 months
`stimulant-use` | Percentage of those in an age group who used stimulants in the past 12 months
`stimulant-frequency` | Median number of times a user in an age group used stimulants in the past 12 months
`meth-use` | Percentage of those in an age group who used meth in the past 12 months
`meth-frequency` | Median number of times a user in an age group used meth in the past 12 months
`sedative-use` | Percentage of those in an age group who used sedatives in the past 12 months
`sedative-frequency` | Median number of times a user in an age group used sedatives in the past 12 months

