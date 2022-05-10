https://blog.analytics-toolkit.com/2017/statistical-significance-ab-testing-complete-guide/

# Statistical Significance in A/B Testing – a Complete Guide

## Understanding random variability

Knowing which actions lead to improvements is not a trivial task, however. 
This is where A/B testing comes into play. 
An A/B test, a.k.a. online controlled experiment, 
is the only scientific way to establish a causal link between our (intended) action(s) and any observed results.

In A/B testing the limit is the time to make a decision and the resources and users one can commit to any given test.

## What is statistical significance?

Statistical significance is a tool which allows action to be taken despite random uncertainty. 
It is a threshold on a statistic called a p-value.
Statistical significance is useful in quantifying uncertainty.

Statistical significance measures how likely it would be to observe what was observed,
assuming the null hypothesis is true.

Statistical significance is then a proxy measure of the likelihood of committing the error of deciding that 
the statistical null hypothesis should be rejected, when in fact, one should have refrained from rejecting it. 
This is also referred to as a type I error, or an error of the first kind. 
A higher level of statistical significance means there are more guarantees against committing such an error.

## What does it mean if a result is statistically significant?

A low p-value means a low probability of an outcome, or a more extreme one, to have occurred. 
Passing a low statistical significance threshold tells us that under the assumptions of the null hypothesis 
(e.g. the true effect is negative or zero) something very unlikely has occurred. 
Logically, observing a statistically significant outcome at a given level can mean that either one of these is true:

1.) There is a true improvement in the performance of our variant versus our control.
2.) There is no true improvement, but a rare outcome happened to be observed.
3.) The statistical model is invalid (does not reflect reality).

It is usually recommended to examine both the p-value and 
a confidence interval to get a better understanding of the uncertainty surrounding any A/B test results.

## Significance in non-inferiority A/B tests

While many online controlled experiments are designed as superiority tests, that is: 
the error of greater concern is that a design, process, etc. that is not superior to the existing one will be implemented, 
there is a good proportion of cases where this is not the error of primary concern. 
Instead, the error that one is trying to avoid the most is that of failing to implement a non-inferior solution.

## Common misinterpretations of statistical significance

### 1. Treating low statistical significance as evidence (by itself) that there is no improvement

In order to reliably measure the uncertainty attached to a claim of no improvement, 
the statistical power of the test should be examined. 
Statistical power measures the sensitivity of the test to a certain true effect, that is: 
how likely the test is to detect a real discrepancy of a certain magnitude at a desired statistical significance level. 
(“Power analysis addresses the ability to reject the null hypothesis when it is false” (sic) [2])

### 2. Confusing high statistical significance with substantive or practically relevant improvement

This is erroneous, since a statistically significant result can be for 
an outcome so small in magnitude that it has no practical value. 

### 3. Treating statistical significance as the likelihood that the observed improvement is the actual improvement

Having such a certainty would usually require much, much more users or sessions.

To get a measure of how big and how small a difference can be expected, 
it is best to examine the confidence intervals around the observed value.

### 4. Treating statistical significance as the likelihood that the alternative hypothesis is true or false

This is a common misconception, which gets especially bad if mixed with misinterpretation #3. 

## Common mistakes in using statistical significance in A/B testing

### 1. Lack of fixed sample size or unaccounted peeking
This mistake happens when:

* using a simple significance test to evaluate data on a daily/weekly/etc. basis, stopping 
once a nominally statistically significant result is observed. 
* the sample size has been decided in advance, but peeking with the intent to stop happens regardless
* using a proper sequential testing method, but failing to register your observations faithfully, so that the statistics can be adjusted accordingly
* using a Bayesian sequential testing method that claims immunity to optional stopping 

#### How to avoid peeking / optional stopping issues?

One way is to fix the sample size in advance and stick to just a single observation at the end of a test. 

### 2. Lack of adjustments for multiple testing

Multiple testing, also called multivariate testing or A/B/n testing, 
is when more than one variant is tested against a control in a given test.

### 3. Lack of adjustments for multiple comparisons

Multiple comparisons happen when there is more than one endpoint for a test.

## How to choose an appropriate statistical significance level (and sample size)?

My advice is to weigh the costs for designing, preparing and running the A/B test against the potential benefits 
(with a reasonable future extrapolation, e.g. several years) and see the sample sizes (and thus time) 
required by several different combinations of values for the three main parameters (significance, power, minimum effect size). 
Then, choose a statistical design that hits closest to the perfect balance. 

