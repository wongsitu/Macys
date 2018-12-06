## Identifying the problem
The company Macy's has started a email advertisement campaign. To test the effectiveness of the results, the company selected a sample size of people, divided them in two groups (TEST and CTRL) and sent each group a respective type of email.

Because the emails from CTRL and TEST were sent simultaneously, we can safely assume that we are working with two independent groups (This also helps to prevent bias results), therefore, we can say that we are conducting a Two-sample t test.

## Data timeline
The data provided covers the dates ranging from June 6th to July 15th of 2017. Some important holidays that took place were:

```
    Father's day => June 18
    Independence's day => July 4
```
It should not be a surprise if we see sales spikes in the provided data. Although, one could think that by including holidays we wouldn't be measuring the raw marketing power of advertisment emails, this thought is most often wrong. Holidays are inheretly part of an economic year. In the U.S, 25% of sales happend in Black Friday, so it's perfectly fine to include these outside factors in our data. We just need to recognize them.

## Asumptions
1. The question does not define the concept of "winner". So, here we can make an assumption (for the sake of simplicity and other reasons, which I will, later, explain why) where the best model has the email that is most likely to be opened. Of couse, this could vary into many alternatives such as: profit generated per email, profit generated per opened email, success rate of openings, success rate of clicked ones, succes rate of orders, etc.

2. Conditions for inference are met, those are: the random condition, the normal condition, the independent condition.

```
- Random: The data needs to come from a random sample or randomized experiment.
- Normal: The sampling distribution of p needs to be approximately normal — needs at least 10 expected successes and 10 expected failures.
- Independent: Individual observations need to be independent. If sampling
without replacement, our sample size shouldn't be more than 10% of the population.
```

3. Significance value of a = 0.05

## Hipothesis

```
Null Hypothesis: The propensity model (CTRL) gives the same results as the engagement models (TEST)
Alternate hypothesis: The engagement models (TEST) surpases the propensity model (CTRL)
```
## Statistics and Progression walkthough



## Findings

Open ratio = open emails/total emails sent,  alpha = 0.001 => Refuted Null hipothesis

Propensity models (CTRL) on average generates more revenue. With the given data, engagement models produces 0.01 cents less than the propensity models. 

Engagement models (TEST) does a better job at attracting customers attention. (Evidenced in alpha test < 0.05)

## Technologies used

```
- Python 2.7
- numpy
- scipy
- csv
```

