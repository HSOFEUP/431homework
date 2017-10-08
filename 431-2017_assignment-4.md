431 Assignment 4
================
Thomas E. Love
Due **2017-10-20** at noon. Version: 2017-10-07

-   [Setting up Questions 1-6 - Using the Formula for Decoding Health News](#setting-up-questions-1-6---using-the-formula-for-decoding-health-news)
    -   [Question 1](#question-1)
    -   [Question 2](#question-2)
    -   [Question 3](#question-3)
    -   [Question 4](#question-4)
    -   [Question 5](#question-5)
    -   [Question 6](#question-6)
-   [Setting up Questions 7 and 8 - Specifying a Two-Sample Study Design](#setting-up-questions-7-and-8---specifying-a-two-sample-study-design)
    -   [Question 7](#question-7)
    -   [Question 8](#question-8)
-   [Setting up Questions 9-11](#setting-up-questions-9-11)
    -   [Question 9](#question-9)
    -   [Question 10](#question-10)
    -   [Question 11](#question-11)

Please review the General Information provided in [Assignment 1](https://github.com/THOMASELOVE/431homework/blob/master/431-2017_assignment-1.md), as well as on [the Main Homework page](https://github.com/THOMASELOVE/431homework) and in the [Course Syllabus](https://thomaselove.github.io/431syllabus/)

Setting up Questions 1-6 - Using the Formula for Decoding Health News
=====================================================================

Find a headline from the internet related to health or medicine that describes the findings of a study published on January 1, 2014 or later. Then find the study being referred to in PUBMED. Use the [formula for updating your opinions about health news developed by Jeff Leek](http://fivethirtyeight.com/features/a-formula-for-decoding-health-news/) we discussed in class, along with the abstract and full contents of the published study to complete Questions 1-6.

Question 1
----------

Specify the URL where we can see the headline and news story describing the findings of the study. Feel free to use `goo.gl` or a related tool online to produce a shortened URL for this purpose. Specify the reference completely, including the names of the author(s) of the news story, and its full title, and source.

Question 2
----------

Specify a URL where we can see at least the abstract of the complete study. Again, shortened URLs are fine. Give the complete reference to the study, as well, including the authors, full title, journal name and so forth.

Question 3
----------

Describe, in a few sentences, your original opinion (gut feeling) related to the conclusions of the study as summarized in the headline and news article, first in terms of a probability statement, and then calculate the appropriate odds, remembering to convert statements about probabilities to statements about odds. Provide some motivation for your internal prior probability, describing your relevant personal experiences or other factors that drove your gut feeling.

Remember, if X is an event, and Pr(X) is the probability that X occurs, and odds(X) are the odds that X occurs, then Pr(X) = odds(X) / (1 + odds(X)) and odds(X) = Pr(X) / (1 - Pr(X)).

Question 4
----------

Evaluate the study in terms of the six specifications [proposed by Leek](http://fivethirtyeight.com/features/a-formula-for-decoding-health-news/) when evaluating study support. Be sure to specify your conclusion about **each** of the six specifications, and provide direct quotes and summarize the evidence from the abstract or paper to address the issues raised and justify your conclusions.

Question 5
----------

Incorporate the study support assessment into a Bayes' Rule calculation to obtain the final odds you should now be willing to give to the headline, and specify this value in terms of a probability statement, as well.

Question 6
----------

React to the final conclusion specified by this approach in a sentence or two. How does your subjective posterior probability that the headline is true match up with the formula's conclusions? Do you feel that the formulaic approach has yielded an appropriate conclusion for you in this case? Why or why not?

Setting up Questions 7 and 8 - Specifying a Two-Sample Study Design
===================================================================

Questions 7 and 8 will ask you to respond (in complete sentences) to several sub-items for the studies described below.

-   \[A\] What is the outcome under study?
-   \[B\] What are the (in this case, two) treatment/exposure groups?
-   \[C\] Were the data collected using matched / paired samples or independent samples?
-   \[D\] Are the data a random sample from the population(s) of interest? Or is there at least a reasonable argument for generalizing from the sample to the population(s)?
-   \[E\] What is the significance level (or, the confidence level) we require here?
-   \[F\] Are we doing one-tailed or two-tailed testing/confidence interval generation?
-   \[G\] If we have paired samples, did pairing help (to reduce nuisance variation)?
-   \[H\] If we have paired samples, what does the distribution of sample paired differences tell us about which inferential procedure to use?
-   \[I\] If we have independent samples, what does the distribution of each individual sample tell us about which inferential procedure to use?

Question 7
----------

For 10 diabetic adults treated with a special diet, the fasting blood sugar values (in mg/dl) before and after treatment were as shown below.

| Person | A   | B   | C   | D   | E   | F   | G   | H   | I   | J   |
|--------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Before | 340 | 335 | 220 | 285 | 320 | 230 | 190 | 210 | 295 | 270 |
| After  | 290 | 315 | 250 | 280 | 311 | 213 | 200 | 208 | 279 | 258 |

In question 7,

-   Describe the entire study using the standard questions above for describing the study design when comparing two samples. You should be responding here to Parts A-F and also either G-H *or* I, whichever is appropriate.
-   As Part J for Question 7, determine whether a statistically significant (*α* = .05) change occurred after treatment. Include in your response evidence supporting any assumptions you make, and an appropriate confidence interval estimate.

Question 8
----------

One of the problems in the study of SIDS is the lack of a good animal model. Baak and Huber (1974) studied the guinea pig as a possible model observing the effect of lethal histamines shock on the guinea pig thymus. The purpose was to determine if changes in the thymus of the guinea pig correspond to pathological changes observed in SIDS victims. In the experiment, 40 animals (20 male, 20 female) were randomly assigned either to "control" or to "histamine shock." The data are gathered in the table below. Note that we will ignore the sex information in this Assignment.

<table>
<colgroup>
<col width="8%" />
<col width="45%" />
<col width="46%" />
</colgroup>
<thead>
<tr class="header">
<th align="right">Sex</th>
<th align="center">Control</th>
<th align="center">Histamine Shock</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="right">Female</td>
<td align="center"><code>6.4 6.2 6.9 6.9 5.4 7.5 6.1 7.3 5.9 6.8</code></td>
<td align="center"><code>8.4 10.2 6.2 5.4 5.5 7.3 5.2 5.1 5.7 9.8</code></td>
</tr>
<tr class="even">
<td align="right">Male</td>
<td align="center"><code>4.3 7.5 5.2 4.9 5.7 4.3 6.4 6.2 5.0 5.0</code></td>
<td align="center"><code>7.5 6.7 5.7 4.9 6.8 6.6 6.9 11.8 6.7 9.0</code></td>
</tr>
</tbody>
</table>

In question 8,

-   Describe the entire study using the standard questions above for describing the study design when comparing two samples. Again, you should be responding here to Parts A-F and also either G-H *or* I, whichever is appropriate.
-   As part J for Question 8, on the basis of the most appropriate 95% confidence interval, ignoring possible sex differences, can you conclude that the tabulated variable \[medullary blood vessel surface (in mm^2 / mm^3)\] differs significantly between "control" and "histamine shock?" Justify the assumptions behind your choice of inference.

Setting up Questions 9-11
=========================

Kapitulnik et al. (1976) compared the metabolism of a drug, zocazolamine, in placentas from 13 women who smoked during pregnancy and 11 who did not. The purpose of the study was to investigate the presence of the drug as a possible proxy for the rate at which benzo\[a\]pyrene (a by-product of cigarette smoke) is metabolized. The data in the `zocazo.csv` file show the measurements of zocazolamine hydroxylase production (nmol 3H2O formed / g per hour) for the 24 subjects.

Question 9
----------

Develop a 99% confidence interval for the difference in the true means of zoxazolamine hydroxylase production in placentas from women who smoked as compared to those who did not, assuming that the distributions of production are approximately Normally distributed in each group.

Question 10
-----------

Suppose that in a new study, we assume a minimum clinically important effect 20% as large as was seen in the Kapitulnik study, and we assume a standard deviation of 1.5. If each individual measurement costs $150 to obtain, how much money will be required to do the study with 99% confidence and 90% power?

Question 11
-----------

Suppose our maximum allowable budget is $15,000 for the study. Comment on whether we can still do the study described in the previous question if we switched to a 95% confidence level.
