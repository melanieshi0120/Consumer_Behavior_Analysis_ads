# Title: Consumer Behavior Analysis - Advertising Project
# Goal: Based on the Consumer behavior data to predict who is more likely to click the ad!
#  Consumer Behavior
![images/consumer_behavior.jpg](images/consumer_behavior.jpg)
## What is Customer Behavior?
consumer behaviour is the study of individuals, groups, or organizations and all the activities associated with the purchase, use and disposal of goods and services, and how the consumer's emotions, attitudes and preferences affect buying behaviour. Scource: https://en.wikipedia.org/wiki/Consumer_behaviour

## What affect consumer behavior?
Making desicions are very dynamic processing and a lof of things could affect consumer behavior. Analyzing the consumer behaviour data are allowed us to present products or services in a way that generates maximum impact on consumers. Consumer behavior is often influenced by different factors such as:
- Personal factors: a specific characteristic such as age, race, gender, culture, income, personal habit/interest, etc
- Psychological factors: an individual’s response to a marketing message will depend on their perceptions and attitudes.
- Company Website: web design, products' reviews from other users, recommendation System 
- Company‘s physical store service
- Social: Policy, Goverment, Economy, Competitors, World of mouth, Friedns and Family etc
- Advertising: Email, Mail, Magazine, Cookie, Social Media, Affiliate(Cashback Website), Partnership (Events like NBA, World Cup, TV Shows)

## Why Consumer Behavior data is important?
Understanding consumer behavior is a vital aspect of marketing. Based on the consumer behavior data, we are able to know how the consumer make decisions and how potential customers will respond to new products or new services. It is important to explore actionable insights from the data to support companies to put forward corresponding strategies.

For example, we do the test (such as AB test, usabiltiy test etc) to gain insights into customer behaviour in order to optimize customer journey and improve key KPIs - Conversion Rate, Revenue, Customer Life Time Value and AOV (Average Order Value)

# Project Introduction
- Dataset Created by Jose Portilla and Pierian Data for his Udemy Course (Python for Data Science and Machine Learning Bootcamp). You can get the data from kaggel -  https://www.kaggle.com/fayomi/advertising .
- The data contains ten differents columns:
    1. Daily Time Spent on a Site -- Time spent by the user on a site in minutes.
    2. Age -- Customer's age in terms of years.
    3. Area Income -- Average income of geographical area of consumer.
    4. Daily Internet Usage -- Avgerage minutes in a day consumer is on the internet.
    5. Ad Topic Line -- Headline of the advertisement.
    6. City -- City of the consumer.
    7. Male -- Whether or not a consumer was male.
    8. Country -- Country of the consumer.
    9. Timestamp -- Time at which user clicked on an Ad or the closed window.
    10. Clicked on Ad -- 0 or 1 is indicated clicking on an Ad or not - 
         Class 0 - not clicked ,and  Class 1 - clicked.
- The goal of this project is to predict what kind of consumers are more likely to click the ad.

# EDA 
## Numertial Data VS Target
 - Based on the image below, we can see that people who spend more time - around 80 minuts on the site are not likely to click the ad, and people who spend around 50 minuts are more likely to click the ad. The average age of the people who clicked the ad is around 40 and the average area income of consumers in class 1 is around 50000. Last, consumers in Class 1 have less daily internet usage. Those subplots are very infomative, and bring us some basic ideas. 
 Besides numerical data, text data can also bring some useful information. For example, what kind of headline or topic of the ad is more attractive and consumers are more likely to click it. 
![images/numertialdata_vs_target.png](images/numertialdata_vs_target.png)

## Text Data
### Bigram
![images/bigram.png](images/bigram.png)
### Word Cloud 
![images/word_cloud_class0.png](images/word_cloud_class0.png)
![images/word_cloud_class1.png](images/word_cloud_class1.png)
People prefer topics like team oriented, fully configuratble, and context sensitive etc. We also can see that some topics that consumers do not really interest.

## Correlationship
- The average age in class 1 is always higher than that in class 0 in every single hour and weekday.
![images/age_vs_target_in_a_day_week.png](images/age_vs_target_in_a_day_week.png)
- The images below show that gender are even in two Classes and both female and male consumers who have lower area income are more likely to click the ad.
![images/gender_hour_weekday.png](images/gender_hour_weekday.png)
- People aged around 40 spend less thant 80 miunts are more likely to click the ad.
- In Class 1, the mean of the age is around 40 and the daily internet usage range is between 100-200.
![images/correlation_pairplot.png](images/correlation_pairplot.png)
- Code Source :https://www.kaggle.com/konchada/logistic-vs-random-forest-model-for-ad-click

## Modeling 
- Random Forest was applied in this project. After tuned hyperparameters with Grid Search and fitted the model, the accuracy and F1 scoure are upto 97%. 
![images/confusion_matrix.png](images/confusion_matrix.png)
![images/ROC.png](images/ROC.png)


- The feature importance chart shows that daily internet usage, daily time spent on site, age and area income playes improtant roles for - "click the ad or not"
![images/feature_importance.png](images/feature_importance.png)


Referece:
- https://www.omniconvert.com/blog/consumer-behavior-in-marketing-patterns-types-segmentation.html
