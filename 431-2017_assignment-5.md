431 Assignment 5
================
Thomas E. Love
Due Thursday **2017-11-09** at noon. Version: 2017-10-08

-   [Question 1 - The Signal and The Noise](#question-1---the-signal-and-the-noise)
-   [Question 2](#question-2)
-   [Question 3](#question-3)
-   [Question 4](#question-4)
    -   [Setup for Questions 5-10](#setup-for-questions-5-10)
-   [Question 5](#question-5)
-   [Question 6](#question-6)
-   [Question 7](#question-7)
-   [Question 8](#question-8)
-   [Question 9](#question-9)
-   [Question 10](#question-10)

Please review the General Information provided in [Assignment 1](https://github.com/THOMASELOVE/431homework/blob/master/431-2017_assignment-1.md), as well as at <https://github.com/THOMASELOVE/431homework> and in the [Course Syllabus](https://thomaselove.github.io/431syllabus/)

Question 1 - The Signal and The Noise
=====================================

Silver writes (in several places prior to Chapter 12, but especially there) that the goal of any predictive model is to capture as much signal as possible and as little noise as possible. What does this mean to you in your scientific and other endeavours, going forward? Give a specific example. An answer of 150 - 250 words is what we're looking for.

Question 2
==========

Suppose you plan to study whether surgery can prolong life among men suffering from prostate cancer, which typically develops and spreads very slowly. Men diagnosed with prostate cancer will be randomly assigned to either undergo surgery or not. Suppose you believe that approximately 10% of men diagnosed with prostate cancer but do not have surgery will eventually die from prostate cancer, and you want to do the study using a sample size that will retain at least 80% power to detect a drop down to 5%, using a two-sided approach with a 95% confidence level.

What is the smallest number of men (including both the surgery and non-surgery groups) that you will need to enroll in this new study to meet these specifications, using a balanced design? Provide the details of your calculation, and also provide a complete sentence or two interpreting the meaning of the results in context.

Question 3
==========

In 2003, the *New England Journal of Medicine* published the results of a Scandinavian study of the issue described in Question 2. In [that report](http://www.nejm.org/doi/10.1056/NEJMoa012794), among 347 men randomly assigned to surgery, 16 eventually died of prostate cancer, compared with 31 of the 348 men who did not have surgery.

With 95% confidence, can you conclude that the odds of death due to prostate cancer is significantly greater for those who did NOT have surgery than it is for those who did have surgery? Provide appropriate details of your calculations, including a sentence or two interpreting the meaning of the results in context.

Question 4
==========

In a 2014 [follow-up report](http://www.nejm.org/doi/full/10.1056/NEJMoa1311593#t=article) describing results at the end of 2012, a total of 63 men assigned to surgery and 99 men not assigned to surgery had died of prostate cancer. In a sentence or two, explain how an analysis of these new results compares to the conclusions you drew in Question 3.

Setup for Questions 5-10
------------------------

A study of the effects of carbon monoxide exposure on men with coronary artery disease subjected the patients to several exercise tests . The men involved in the study were recruited from three different medical centers. Before combining the subjects into one large group to conduct the analysis, we need to first examine whether baseline characteristics of the subjects from the three medical centers (21 from Johns Hopkins University, 16 from Rancho Los Amigos, and 23 from St. Louis University) are comparable. Here, we examine pulmonary function at the start of the study, and we've pre-planned pairwise comparisons across all combinations of the three centers. For each of the 60 subjects, we have a measure of forced expiratory volume in 1 second (FEV<sub>1</sub>, in liters) stored in the `coexpose1.csv` and the `coexpose2.csv` files on [our course website](https://github.com/THOMASELOVE/431homework/tree/master/HW5).

This data set is built from an example in Chapters 11 and 12 of Pagano and Gauvreau. The data source is Allred EN et al. Acute effects of carbon monoxide exposure on individuals with coronary artery disease. Health Effects Institute Research Report Number 25, November 1989.

Question 5
==========

The same data appear in the `coexpose1.csv` and the `coexpose2.csv` files. What is the difference between the two files, and which of the two files is more useful for fitting an ANOVA to compare the FEV<sub>1</sub> means across the three medical centers?

Question 6
==========

Produce a numerical summary to compare the means across the three centers, and specify the rank order (highest to lowest) of the sampled FEV<sub>1</sub> levels.

Question 7
==========

Produce a graphical summary to compare the three centers that allows you to assess the Normality and Equal Variances assumptions of an ANOVA to compare the FEV<sub>1</sub> means across the three medical centers. What conclusion do you draw about the assumptions in this setting?

Question 8
==========

Compare the FEV<sub>1</sub> means of the three different medical centers using an analysis of variance. What conclusion do you draw, using a **90%** confidence level?

Question 9
==========

Specify the linear model regression equation used to predict our FEV<sub>1</sub> outcome on the basis of medical center. What fraction of the variation in FEV<sub>1</sub> levels is explained by the medical center?

Question 10
===========

This is a pre-planned comparison, but the sample sizes differ across the groups being compared. Obtain the results from a Tukey HSD method and then a Bonferroni approach for pairwise comparisons of the population FEV<sub>1</sub> means, in each case again using a 90% confidence level. Do your conclusions differ?

As a hint, note that the `TukeyHSD` function takes a `conf.level` argument to specify something other than the default 0.95. So, in fact, does the Bonferroni approach using `pairwise.t.test`, although it's not actually necessary there, since that method only produces *p* values, not confidence intervals.
