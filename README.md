## Identifying the problem
The company Macy's has started an email advertisement campaign and decided to compare two different versions of email ads. The company selected a sample size of people, divided them in two groups (TEST and CTRL) and sent each group a respective type of email.

Because the emails from CTRL and TEST were sent simultaneously, we can safely assume that we are working with two independent groups (This also helps to prevent bias results), therefore, we can say that we are conducting a Two-sample t test.

## Data timeline
The data provided covers the dates ranging from June 6th to July 15th of 2017. Some important holidays that took place were:

```
    Father's day => June 18
    Independence's day => July 4
```
It should not be a surprise if we see sales spikes in the provided data. Although, one could think that by including holidays we wouldn't be measuring the raw marketing power of advertisment emails, this thought is most often wrong. Holidays are inheretly part of an economic year. In the U.S, 25% of sales happend in Black Friday, so it's perfectly fine to include these outside factors in our data. We just need to recognize them.

## Asumptions
1. The question does not define the concept of "winner". So, here we can make an assumption (for the sake of simplicity and other reasons, which I will later) where the best model has the email that is most likely to be opened. Of couse, this could vary into many alternatives such as: revenue generated per email (RPE), revenue generated per opened email, success rate of openings, success rate of clicked ones, succes rate of orders, etc.

2. Conditions for inference are met, those are: the random condition, the normal condition, the independent condition.

```
- Random: The data needs to come from a random sample or randomized experiment.
- Normal: The sampling distribution of p needs to be approximately normal — needs at least 10 expected successes and 10 expected failures.
- Independent: Individual observations need to be independent. If sampling
without replacement, our sample size shouldn't be more than 10% of the population.
```
4. Some of the data had absurd values such as 100% order success, number of orders were higher than clicks, click pertentages getting higher than 100%, etc. My assumption here is that these are outliers of failed tests due to many reasons. To clean this, we computed the marginal error and filtered them by setting a threshhold of 0.05 (5% error margin). This should not be ground-breaking thanks to the field in which Macys operates.

3. Significance value of a = 0.05

## Introduction

GOAL:
```
Determine which of the advertisement models (Propensity-CTRL or Engagement-TEST) is more effective depending on the tracking metrics.
```
TRACKING METRICS:
```
Open Rate = emails opened/(emails sent - emails bounced)
Click Rate = number of clicks / emails opened
Order Rates = number of orders/ number of clicks
Revenue per email(RPE) = amount of money/(emails sent - emails bounced)

NOTE: emails bounced are the emails who were not sent successfully, since the data does not provide that information, we will assume that
emails bounced = 0 and emails sent = delivered
```
HYPOTHESIS
```
NULL Hypothesis: The propensity model (CTRL) gives the same results as the engagement models (TEST)
Alternate hypothesis: The engagement models (TEST) surpases the propensity model (CTRL)
```

Like a standart A/B testing procedure, we will hold our NULL hypothesis until proven false.

## Statistics and Progression walkthough



## Findings

Open ratio = open emails/total emails sent,  alpha = 0.001 => Refuted Null hipothesis. This means that engagement models (TEST) does a better job at attracting customers attention. (Evidenced in alpha test < 0.05). 

However, when running the double sample independent t test on other categories, it constantly throws back a value higher than 0.05. This means that our TEST model does nothing better than out CTRL model , except for capturing the attention of customers. The main factor, and perhaps, the most probable is that Macy's engagement model's emails do a very good job at capturing the customer's attention. 

Propensity models (CTRL) on average generates more revenue per email (RPE). With the given data, engagement models produces 0.01 cents less than the propensity models. 1 cent might seem small when users are looking a lot more to your advertisement campaigns, but it actually represents a loss 11.7%!

## Technologies used

```
- Python 2.7
- numpy
- scipy
- csv
```

