431 Assignment 6
================
Thomas E. Love
Due **2017-12-01** at noon. Version: 2017-10-08

-   [Question 1](#question-1)
-   [Question 2](#question-2)
-   [General Description of the Data for Questions 3-5](#general-description-of-the-data-for-questions-3-5)
-   [Question 3](#question-3)
-   [Question 4](#question-4)
-   [Question 5](#question-5)
-   [Question 6](#question-6)

Please review the General Information provided in [Assignment 1](https://github.com/THOMASELOVE/431homework/blob/master/431-2017_assignment-1.md), as well as at <https://github.com/THOMASELOVE/431homework> and in the [Course Syllabus](https://thomaselove.github.io/431syllabus/)

Question 1
==========

> It is still standard to display data summaries as tables rather than graphs, even though graphs are typically better suited for perceiving trends and making comparisons and predictions.

> Gelman A and Nolan D, Teaching Statistics: A Bag of Tricks, Second Edition, section 4.6

Find a Wikipedia page with a table that interests you. Scrape the data from the table and clean it up, converting character strings to numbers, dropping unneeded variables, and so forth, leading to a tidy data set in R. Create a statistical graph from these data. Write a caption for your figure that interprets your findings. Be sure to provide the link to the original Wikipedia table.

Question 2
==========

Find an example of a visualization designed to support a linear regression analysis in a published work (online or not) for which you can find the complete sourcing information, and which was built no earlier than January 1, 2014. Provide the complete reference and a copy of the image itself (including any captions or titles) and surrounding material for the visualization, and provide a brief essay (likely to run 150-250 words) which accomplishes each of the following tasks:

1.  Describe the linear regression model behind the visualization. Explain its context and why it is important. Specify the research question that this regression model answers.
2.  Describe the visualization and explain what you believe it is trying to do. Specify why it is or is not effective, in your view.
3.  Provide your best suggestion as to how the visualization might be improved, and explain why your change would be an improvement.

General Description of the Data for Questions 3-5
=================================================

Low dietary intake or low plasma concentrations of retinol, beta-carotene, or other carotenoids might be associated with increased risk of developing certain types of cancer. However, relatively few studies have investigated the determinants of plasma concentrations of these micronutrients. A cross-sectional study was designed to investigate the relationship between personal characteristics and dietary factors, and plasma concentrations of retinol and/or beta-carotene. Study subjects (*n* = 300) were patients who had an elective surgical procedure during a three-year period to biopsy or remove a lesion of the lung, colon, breast, skin, ovary or uterus that was found to be non-cancerous.

<table>
<colgroup>
<col width="23%" />
<col width="76%" />
</colgroup>
<thead>
<tr class="header">
<th align="right">Variable</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="right"><code>id</code></td>
<td>Subject identification number - just a code</td>
</tr>
<tr class="even">
<td align="right"><code>age</code></td>
<td>Subject's age (in years)</td>
</tr>
<tr class="odd">
<td align="right"><code>sex</code></td>
<td>Subject's gender (1 = male, 2 = female)</td>
</tr>
<tr class="even">
<td align="right"><code>smoking</code></td>
<td>Smoking Status (1 = never, 2 = former, 3 = current)</td>
</tr>
<tr class="odd">
<td align="right"><code>bmi</code></td>
<td>Body-Mass Index ( weight in kilograms <span class="math inline">/</span> [height in meters]<span class="math inline"><em></em><sup>2</sup></span> )</td>
</tr>
<tr class="even">
<td align="right"><code>vitamin</code></td>
<td>Vitamin Use (1 = Yes, fairly often, 2 = Yes, not so often, 3 = No)</td>
</tr>
<tr class="odd">
<td align="right"><code>calories</code></td>
<td>Number of Calories consumed (per day)</td>
</tr>
<tr class="even">
<td align="right"><code>fat</code></td>
<td>Number of grams of fat consumed (per day)</td>
</tr>
<tr class="odd">
<td align="right"><code>fiber</code></td>
<td>Number of grams of fiber consumed (per day)</td>
</tr>
<tr class="even">
<td align="right"><code>alcohol</code></td>
<td>Number of alcoholic drinks consumed (per week)</td>
</tr>
<tr class="odd">
<td align="right"><code>cholesterol</code></td>
<td>Number of milligrams of cholesterol consumed (per day)</td>
</tr>
<tr class="even">
<td align="right"><code>betadiet</code></td>
<td>Number of micrograms of dietary beta-carotene consumed (per day)</td>
</tr>
<tr class="odd">
<td align="right"><code>retdiet</code></td>
<td>Number of micrograms of dietary retinol consumed (per day)</td>
</tr>
<tr class="even">
<td align="right"><code>betaplasma</code></td>
<td>Plasma beta-carotene (in ng<span class="math inline">/</span>ml)</td>
</tr>
<tr class="odd">
<td align="right"><code>retplasma</code></td>
<td>Plasma retinol (in ng<span class="math inline">/</span>ml)</td>
</tr>
<tr class="even">
<td align="right"><code>holdout</code></td>
<td>Explained below (1 = hold out, 0 = do not hold out)</td>
</tr>
</tbody>
</table>

The `hw6plasma` data set is available [on our web site](https://github.com/THOMASELOVE/431homework/tree/master/HW6). It contains 300 observations. You will use a subset of 275 of those observations (those for which the `holdout` variable is equal to 0) to fit your models, and a separate sample of the remaining 25 observations (those for which `holdout` = 1) to validate your model selection.

The essential conclusion we are looking to make (if it is true) in the context of these data is as follows:

> We conclude that there is wide variability in plasma concentrations of these micronutrients in humans, and that much of this variability is associated with dietary habits and personal characteristics.

Your fundamental task is to produce and interpret a series of appropriate statistical models to help us decide whether or not these conclusions are reasonable, in the case of plasma retinol, in particular. The most important thing is to accurately reflect [the data you have received](https://github.com/THOMASELOVE/431homework/tree/master/HW6).

Question 3
==========

Build and specify a model for plasma retinol. Specify whether a transformation of the outcome is necessary, and how you know. If you need a transformation, specify a wise choice. Select predictors from the demographic, behavioral and relevant dietary factors described in the data (i.e. not including `id, betadiet, betaplasma` or `holdout`.) Motivate your choice of predictors, including an assessment of the impact of collinearity, with appropriate accounting for it in your final choice of model. Specify and demonstrate the impact of your model selection algorithm. For questions 3-5, use only the **275 observations** where `holdout` is 0.

Question 4
==========

Summarize the findings in a clear presentation of your final model, including a short recap of the steps you took to produce it. Demonstrate the utility of the final model, including summaries based on *R*<sup>2</sup> and significance testing. Demonstrate that your final model passes required checks of assumptions. For questions 3-5, use only the **275 observations** where `holdout` is 0.

Question 5
==========

In a single sentence, outline the key findings for plasma retinol specified by your model.

Question 6
==========

At this point, we will return to working with the whole set of 300 observations. Validate your choice of model for plasma retinol level by using your final choice developed in questions 3-5 to predict data for the 25 cases that you have withheld from the data, comparing your final model to these two other models:

-   A model using `age` and `sex` alone.
-   A model that uses the entire set (kitchen sink) of possible predictors, i.e. everything but `id`, `betadiet` and `betaplasma`.

Which model looks best in your comparison? Justify your response.
