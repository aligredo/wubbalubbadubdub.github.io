# Wubba Lubba Dub Dub!

## Who Are We?
A team of students enrolled in Data Engineering course at The German University in Cairo teached and supervised by [Assoc. Prof. Mervat Abuelkheir](http://met.guc.edu.eg/People/Profile.aspx?facId=3179 "MET website profile").
### Team Members
- Engy Fawaz
- Dina Hisham
- Mohamed Maher
- Wessam Ali
- Ali Ahmed

## Overview and Motivation 
The Android applications market has been very competetive with a lot of available applications in various categories. Therefore, it is very important to have full understanding of the market needs before developing an application. Our goal is to construct a business guideline for developing  an application and publishing it to the market which is the Google Play Store. Moreover, one of the most important reasons that inspired us to analyze the Google Android Store is that a member of the team is a game developer who has a game application published on Google Android Store and we were curious how could we reach highest success for this game application.

## Initial Questions
1. Which app type is most commonly added to Android Store (Free vs Paid)?
1. Is there a relation between Ratings and Category?
1. Is there a relation between Ratings and Type?
1. Which category of Apps are most commonly not free to install?
1. Are paid apps downloaded as much as free apps?
1. Is there a relationship between the number of reviews and the number of installs?
1. Is there a relationship between ratings values and the app size?
1. Who are the targeted users across categories?
1. Is there a relation between last update of the application and number of installs?

## Data
[The Android App Market on Google Play](https://www.datacamp.com/projects/619), Web scraped data of 10k Play Store apps for analysing the Android market.

## Data Preprocessing
A walkthrough our data preprocessing process to ensure that our results is based on clean and credible data.

### Pipeline
Visualization of our preprocessing for the data set.
![Image](https://github.com/aligredo/wubbalubbadubdub.github.io/blob/master/Data/Preprocessing%20Sequence.png "Data Preprocessing Pipeline")

### Handling Duplicate Values
We found out that the number of rows is greater than the number of apps, which intuitively implies that there are duplicate values in the data set, so we decided to drop the duplicate rows from our data set.

### Handling Messing Values
We found 1481 missing rows that have missing values in them. We could not afford dropping all those apps data, since they represent about 15% of the whole data set. As most of the missing values were from the ratings column -about 99%- we decided to put the mean of ratings of the application's category, however since the rest of the missing values were too few we decided to get them manually from the Play Store. Finally we had only 12 records that we were unable to replace the null values appropriately, for those we decided to drop them.

### Feature Engineering 
We removed the '$' from the price column and '+' form the downloads column to be able to perform analysis easily on both of those columns, and we renamed the columns to match the new type of the values. Futhermore, we created a new column which represents the number of days passed since the last update was released for that app in order to make it easier for our analysis process.




