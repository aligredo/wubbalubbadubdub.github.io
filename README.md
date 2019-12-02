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
![Image](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/Preprocessing%20Sequence.png "Data Preprocessing Pipeline")

### Handling Duplicate Values
We found out that the number of rows is greater than the number of apps, which intuitively implies that there are duplicate values in the data set, so we decided to drop the duplicate rows from our data set.

### Handling Missing Values
We found 1481 missing rows that have missing values in them. We could not afford dropping all those apps data, since they represent about 15% of the whole data set. As most of the missing values were from the ratings column -about 99%- we decided to put the mean of ratings of the application's category, however since the rest of the missing values were too few we decided to get them manually from the Play Store. Finally we had only 12 records that we were unable to replace the null values appropriately, for those we decided to drop them.

### Feature Engineering 
We removed the '$' from the price column and '+' form the downloads column to be able to perform analysis easily on both of those columns, and we renamed the columns to match the new type of the values. Futhermore, we created a new column which represents the number of days passed since the last update was released for that app in order to make it easier for our analysis process.

## Data Analysis And Results

### Which app type is most commonly added to Android Store (Free vs Paid)?
We visualized the number of the free apps versus the paid apps on the Play Store.

![plot1](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot1.png "Free vs. Paid Apps")

As observed about 85% of the apps on the store are free while the rest are paid apps.

### Is there a relation between Ratings and Category?
Using box-plots we visualized the mean of ratings for each category in our data set.

![plot2](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot2.png "Category-Rating Box-plots")

Obviously, we can see that all categories in android store have similar mean values of ratings. We can also observe that Event Apps have the highest ratings mean while Dating Apps have lowest ratings mean.

### Is there a relation between Ratings and Type?
Also Using box-plots we were able to conclude that both free and paid values have close mean values.

![plot3](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot3.png "Paid vs Free Ratings")

### Which category of Apps are most commonly not free to install?
We visualized the percentage of the paid apps of each category.


![plot4](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot4.png "Paid Percentage")

We can see that the percentage of paid apps is peaking in medical and personalization categories. Interestingly, we found out that the highest number of installs in paid apps are in communication, social and video players categories. And surprisingly the number of installs for medical and personalization paid apps are really very low!

![plot5](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot5.png "Paid Downloads")

### Are paid apps downloaded as much as free apps?
Using box-plot we found out that the mean of minimum downloads for paid apps are significantly less than for free apps.

![plot6](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot6.png "Paid vs Free Minimum Downloads")

### Is there a relationship between the number of reviews and the number of installs?
We plotted the correlation between the number of reviews and the number of installs.

![plot7](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot7.png "Review and  Installs Correlation")

There is a positive correlation between the number of reviews and the number of installs. As the number of reviews increasem, the number of minimum installs increases.Thus, this correlation shows that users tend to install apps that are reviewed by a large number of people. Moreover, this can also mean that a considerable amount of users give feedbacks or reviews after installing an app.

### Is there a relationship between ratings values and the app size?
The scatter plot shows a condensation between the high ratings (3.5 - 5.0) and the small app sizes (between roughly 5M till 18M), for paid apps. Concluding that, most of the paid apps in the Android Store with high ratings, are of small sizes. This could refer that for a more successful paid app, it is advisable to consider the size to be relatively small.

![plot8](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot8.png "Size and Rating Scatter Plot")

### Who are the targeted users across categories?
From this multiple bar chart, we can see who are the application targeted audience according to each category.

![plot9](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot9.png "Target Audience")

### Is there a relation between last update of the application and number of installs?

This Line-plot shows that there is a positive relation between frequency of updating applications and number of installs.

![plot10](https://raw.githubusercontent.com/aligredo/wubbalubbadubdub.github.io/master/Data/plot10.png "Updates and Downloads")

## And That's All You Need To Know Before You Start Developing Your APP!
