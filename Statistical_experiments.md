https://learning.oreilly.com/library/view/improve-the-outcome/9781491978351/ch01.html

# Statistical Experiments and Significance Testing

<img src="https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781491978351/files/assets/Inference-pipeline.png">

## A-B Testing

```
An A-B test is an experiment with two groups to establish which of two treatments, products, procedures, etc., is superior. 
```
Often, one of the two treatments is the standard existing treatment, or no treatment. 
If a standard (or no) treatment is used, it is called the control. 
A typical hypothesis is that treatment is better than control.

```
KEY TERMS FOR A-B TESTING

* Treatment
Something (drug, price, web headline) to which a subject is exposed

* Treatment group
A group of subjects exposed to a specific treatment

* Control group
A group of subjects exposed to no (or standard) treatment

* Randomization
The process of randomly assigning subjects to treatments

* Subjects
The items (web visitors, patients, etc.) that are exposed to treatments

* Test statistic
The metric used to measure the effect of the treatment
```

A-B tests are common in web design and marketing, since results are so readily measured.

### BLINDING IN STUDIES

A blinded study is one in which the subjects are unaware of whether they are getting treatment A or treatment B. 
Awareness of receiving a particular treatment can affect response. 
A double blind study is one in which the investigators and facilitators 
(e.g., doctors and nurses in a medical study) are unaware which subjects are getting which treatment. 
Blinding is not possible when the nature of the treatment is transparent—e.g., cognitive therapy from a computer versus a psychologist.

### KEY IDEAS

Subjects are assigned to two (or more) groups that are treated exactly alike, except that the treatment under study differs from one to another.
Ideally, subjects are assigned randomly to the groups.

## Hypothesis tests
Hypothesis tests, also called significance tests, are ubiquitous in the traditional statistical analysis of published research. Their purpose is to help learn whether random chance might be responsible for an observed effect.

### KEY TERMS

#### Null hypothesis
The hypothesis that chance is to blame
No difference between the means of group A and group B
A ≤ B
B is not X% greater than A

#### Alternative hypothesis
Counterpoint to the null (what you hope to prove)
“A is different from B” (could be bigger or smaller)
B > A
B is X% greater than A

#### One-way test
Hypothesis test that counts chance results only in one direction
B is better than A

#### Two-way test
Hypothesis test that counts chance results in two directions
A is different from B, could be bigger or smaller

KEY IDEAS
A null hypothesis is a logical construct embodying the notion that nothing special has happened, 
and any effect you observe is due to random chance
The hypothesis test assumes that the null hypothesis is true, creates a “null model” (a probability model) 
and tests whether the effect you observe is a reasonable outcome of that model

