## Identifying the problem
The company Macy's has started a email advertisement campaign. To test the effectiveness of the results, the company selected a sample size of people, divided them in two groups (TEST and CTRL) and sent each group a respective type of email.

Because the emails from CTRL and TEST were sent simultaneously, we can safely assume that we are working with two independent groups (This also helps to prevent bias results), therefore, we can say that we are conducting a Two-sample t test.

## Data timeline
The data provided covers the dates ranging from June 6th to July 15th of 2017. Some important holidays that took place were:

```
    Father's day => June 18
    Independence's day => July 4
```
It should not be a surprise if we see sales spikes in the provided data.

## Asumptions
Conditions for inference are met, those are: the random condition, the normal condition, the independent condition.

Significance value of a = 0.05

The question does not define the concept of "winner" of "best model". So, here we can make an assumption where the best model is the one that generates the most revenue per email. 

```
- Random: The data needs to come from a random sample or randomized experiment.
- Normal: The sampling distribution of p needs to be approximately normal — needs at least 10 expected successes and 10 expected failures.
- Independent: Individual observations need to be independent. If sampling
without replacement, our sample size shouldn't be more than 10% of the population.
```

## Hipothesis

```
Null Hypothesis: The propensity model (CTRL) gives the same results as the engagement models (TEST)
Alternate hypothesis: The engagement models (TEST) surpases the CTRL model
```

## Technologies used

```
- Python 2.7
- numpy
- scipy
- csv
```

