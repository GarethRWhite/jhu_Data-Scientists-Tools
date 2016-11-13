#Types of Data Science Questions

In order of increasing difficulty to achieve the goal of analysis:

*Descriptive
*Exploratory
*Inferential
*Predictive
*Causal
*Mechanistic

## Descriptive
Goal: Describe set of data
Descriptions can usually not be generalized without additional statistical models.
e.g.,
http://www.census.gov/2010census

http://books.google.com/ngrams

## Exploratory
Goal: Find relationships you didn't know about
But not necessarily confirm them
Useful for defining future studies
Shouldn't be used for generalizaing or predicting.
http://www.sdss.org/

## Inferential
Goal: Take small set of data and generalize to larger population
Most common goal of statistical models
Estimate quantity you're interested in, and your uncertainty about it.
e.g.,
Effect of Air Pollution Control on Life Expectancy in the United States: An Analysis of 545 U.S. Countines

## Predictive
Goal: Use data on some objects to predict values for another object.
Even if x predicts y, it does not mean that X causes Y
More data and a smiple model works well.
Prediction is very hard, especially about the future.
e.g.,
http://fivethirtyeight.blogs.nytimes.com

http://www.forbes.com/sites/kashmirhill/2012/02/16/how-target-figured-out-a-teen-girl-was-pregnant somethig blah

## Causal
Goal: find out what happens to one variable when you make another variable change
Usually randomized control trials required to identify causation
Usually identified as average effects, but may not apply to all individuals.
The goal standard for analyses types.

## Mechanistic
Goal: Understand the exact changes in variables that lead oto changes in other variables for individual objects.
Incredibly hard to infer, except in simple situations.
Usually modelled by deterministic set of equations (physical / engineering)
The only random component is measurement error
If the equations are known but parameters are not, they may be inferred with data analysis.
e.g.,
http://fhwa.dot.gov/resourcecenter/teams/pavement/pave_3pdg.pdf




# What is Data?

Data are values of qualitative or quantitative varialbes, belonging to a set of items.
http://en.wikipedia.org/wiki/Data

Data: Set of items: sometimes called the population
Variables: a measurement or characteristic of an item.
Qualitative: Country of origin, sex, treatment
Quantitative: Height, weight, blood pressure (continuous scale, ordering, etc.)

e.g.,
http://brianknaus.com/software/srtoobox/s_4_1_sequence80.txt
https://dev.twitter.com/docs/api/1/get/blocks/blocking
http://blue-button.github.com/challenge/
http://www.nytimes.com/2012/06/26/technology/in-a-big-network-of-computers-evidence-of-machine-learning.html
http://www.pnas.org/content/109/30/12081.full
https://soundcloud.com/uncoolbob/sets/darwintunes
http://www.data.gov/

Data is second most important thing.
First is the question you're trying to answer.
Data will limit or enable the question you're trying to ask.
Having the data can't save you if you don't have a question.



# What about Big Data?

http//mashable.com/2011/06/28/data-infograhic/
http://www.chrisstucchio.com/blog/2013/hadoop_hatred.html
"Don't use Hadoop - your data isn't that big"

"The data may not contain the answer. The combination of some data an an aching desire for an answer does not ensure that a resonable ansswwer can be extracted"
"... no matter how big the data are."



# Experimental Design

Original result
http://www.nature.com/nm/journal/v12/n11/full/nm1491.html
Refutation
http://arxiv.org/pdf/1010.1092.pdf

nsaunders.wordpress.com/2012/07/23/we-really-dont-care-what-statistical-method-you-used

##Have a plan for data and code sharing
https://github.com/
http://figshare.com/
https://github.com/jtleek/datasharing

## Formulate your question in advance
http://www.wired.com/business/2012/04/ff_abtesting

## Statistical Inference
http://www.gs.washington.edu/academics/courses/akey/56008/lecture/lecture2.pdf

## Variability - Scenario1
X axis: Webpage version: Sign-up; Donate
Y axis: Dollars (thousands)

High variability in both versions.

## Variability - Scenario 2

Very small variability within each version.
Very small difference between both.


## Variability - Scenario 3

Very small variability within each version.
Very large difference between both.

## Confounding
Shoe size
Literacy
Looking for correllations
Perhaps people with small shoe sizes have low literacy.
Age is a counfounding varialbe. When you're young your shoes and literacy are small.
What are the other variables that might be causing the relaionship....?

## Correlation is not causation
http://www.nejm.org/doi/full/10.1056/NEJMon1211064
Correlation between chocolate consumption and number of Nobel laureates per captia.
Perhaps due to higher GDP?

Spurious causation.

## Randomization and blocking
Fix a variable. e.g., both websites say "Obama 2014".
If you don't fix, then stratify. If you are testing sign up phrases and have two colors, use both phrases equally on both colors.
If you can't fix a variable, randomize it.

## Why does randomization help?

www.gs.washington.edu/academics/courses/akey/56008/lecture/lecture1.pdf

Confounding variables are spread through all treatments.


## Prediction
Observations from the sample, 2 gropus, responders or not responders to treatmetn.

## prediction versus inference

http://www.biostat.jhsph.edu/~iruczins/teaching/140.615

Prediction needs distributions to be more separated, so observations can clearly be determined to be from one population or the other.

## Prediction key quantities

             Have Disease
        +                   -

Test
+     True positive    False positive
-     False negative   True negative

Pr (x | y)
Probability of x given y

*Sensitivity -> Pr (positive test | disease)
*Specificity -> Pr (negative test | no disease)
*Positive predictive value -> Pr (disease | positive test)
*Negative predictive value -> Pr (no disease | negative test)
*Accuracy -> Pr (correct outcome)

http://www.biostat.jhsph.edu/~iruczins/teaching/140.615

## Beware data dredging
http://xkcd.com/882/

Could chagne hypothesis, until you find a result you like.
Repeated trials.

## Summary
Good experiments:
Have replicability
Measure variability
Generalize to the problem you care about
Are transparent (code and data).

Prediction is not inference:
Both can be important

Beware data dredging.

