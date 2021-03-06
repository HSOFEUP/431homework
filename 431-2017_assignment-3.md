431 Assignment 3
================
Thomas E. Love
Due **2017-09-29** at noon. Version: 2017-08-27

-   [Question 1 - Fox or Hedgehog?](#question-1---fox-or-hedgehog)
-   [Data for Questions 2-7](#data-for-questions-2-7)
-   [Question 2](#question-2)
-   [Question 3](#question-3)
-   [Question 4](#question-4)
-   [Question 5](#question-5)
-   [Question 6](#question-6)
-   [Question 7](#question-7)

Please review the General Information provided in [Assignment 1](https://github.com/THOMASELOVE/431homework/blob/master/431-2017_assignment-1.md), as well as at <https://github.com/THOMASELOVE/431homework> and in the [Course Syllabus](https://thomaselove.github.io/431syllabus/)

Question 1 - Fox or Hedgehog?
=============================

In anticipation of this assignment, you've read through Chapters 2 and 3 of Nate Silver's *The Signal and The Noise.*

I'm curious to know if a field you are interested in is more inclined to predicting like a fox or a hedgehog. Can you (briefly, in 200 ± 75 words) describe how a field of interest to you (perhaps your choice of field here should exclude baseball or political punditry, since Nate has covered those well in these chapters) makes its predictions?

To do this, please provide an example from your chosen field of a *typical* presentation of an important conclusion made by a thought leader, with an appropriate citation, and a little context. In your view, are conclusions in your field mostly presented in a probabilistically defensible way, or else with more certainty than perhaps can be supported. Why might this be so?

Data for Questions 2-7
======================

One of the data frames that comes with the base installation of R (technically, as part of the `datasets` package) is the classic Anderson/Fisher *iris* data set, that gives the measurements (in cm) of the sepal length and width and the petal length and width for 50 flowers from each of 3 species of iris. The species are *iris setosa*, *iris versicolor* and *iris virginica*.

For more on the iris data, which has been used as an example in multivariate statistical modeling and data mining courses for decades, you might visit [its Wikipedia page](https://en.wikipedia.org/wiki/Iris_flower_data_set). Yes, of course, this data set has its own Wikipedia page. To look at the data set in R, just type in `iris`. You can and should create a tibble containing the iris data (I suggest using the name `iris1` for your tibble) in the usual way. Then use this tibble to answer questions 2-7.

Question 2
==========

Across the entire sample of 150 flowers, find and interpret the correlation of petal length and petal width. Does it matter much whether you use the Pearson or Spearman correlation?

Question 3
==========

Draw an appropriate scatterplot to assess the prediction of petal length (our *outcome*) using petal width as a predictor. Include both a loess smooth and regression line in your plot. Does the plot suggest that a straight line model is appropriate in this case?

Question 4
==========

Suppose we are interested in which of the three types of iris (*setosa*, *versicolor* or *virginica*) shows the strongest *linear* relationship between petal length and petal width. Draw an attractive and thoughtfully labeled plot of the relevant data to address this issue, accompanied by a sentence or two describing the key findings from your plot. Postpone the discussion of a numerical summary to Question 5.

Question 5
==========

Is the *correlation* between petal length and petal width larger or smaller in the sample of 150 flowers than in the species-specific samples of 50 flowers each? Why does this appear to be the case? On the basis of your correlation, which iris type shows the strongest *linear* relationship for the prediction of petal length on the basis of petal width? Specify the Pearson correlation (to two decimal places) for your strongest model here.

Question 6
==========

Using the strongest model that you identified in question 5, what is the difference in the predicted petal length between two new flowers, one of whom has a petal width at the 75th percentile of the original data for that iris type, and the other of whom has a petal width at the 25th percentile of the original data for that iris type? Be sure to specify which of the two new flowers would be expected to be longer.

Question 7
==========

Using two different approaches, build two gorgeous and thoughtfully labeled plots of the relationship between *sepal length* and *sepal width*, so that each plot distinguishes between the three types of iris. Use color to indicate each iris type, and show color-coded loess smooths (or linear fits, your choice) for each iris type.

What conclusions can you draw about the effectiveness of the two types of plots you've built? Is one clearly better than the other? Why or why not?
