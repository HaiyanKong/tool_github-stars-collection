---
project: FriendsDontLetFriends
stars: 6466
description: Friends don't let friends make certain types of data visualization - What are they and why are they bad. 
url: https://github.com/cxli233/FriendsDontLetFriends
---

Friends Don't Let Friends Make Bad Graphs
=========================================

Friends don't let friends make certain types of data visualization - What are they and why are they bad.

-   Author: Chenxin Li, Ph.D., Assistant Research Scientist at Department of Crop & Soil Sciences and Center for Applied Genetic Technologies, University of Georgia.
-   Contact: Chenxin.Li@uga.edu | @ChenxinLi2 | @chenxinli2.bsky.social

This is an _opinionated_ essay about good and bad practices in data visualization. Examples and explanations are below.

The `Scripts/` directory contains `.Rmd` files that generate the graphics shown below. It requires R, RStudio, and the rmarkdown package.

-   R: R Download
-   RStudio: RStudio Download
-   rmarkdown can be installed using the install packages interface in RStudio

Table of contents
=================

1.  Friends Don't Let Friends Make Bar Plots For Mean Separation
2.  Friends Don't Let Friends Make Violin Plots for Small Sample Sizes
3.  Friends Don't Let Friends Use Bidirectional Color Scales for Unidirectional Data
4.  Friends Don't Let Friends Make Bar Plot Meadow
5.  Friends Don't Let Friends Make Heatmap without Reordering Rows & Columns
6.  Friends Don't Let Friends Make Heatmap without Checking Outliers
7.  Friends Don't Let Friends Forget to Check Data Range at Each Factor Level
8.  Friends Don't Let Friends Make Network Graphs without Trying Different Layouts
9.  Friends Don't Let Friends Confuse Position and Length Based Visualizations
10.  Friends Don't Let Friends Make Pie Charts
11.  Friends Don't Let Friends Make Concentric Donuts
12.  Friends Don't Let Friends Use Red/green and Rainbow for Color Scales
13.  Friends Don't Let Friends Forget to Reorder Stacked Bar Plot
14.  Friends Don't Let Friends Mix Stacked Bars and Mean separation

1\. Friends Don't Let Friends Make Bar Plots for Means Separation
=================================================================

This has to be the first one. Means separation plots are some of the most common in scientific publications. We have two or more groups, which contains multiple observations; they may have different means, variances, and distributions. The task of the visualization is to show the means and the spread (dispersion) of the data.

In this example, two groups have similar means and standard deviations, but quite different distributions. **Are they really "the same"?** Just don't use bar plot for means separation, or at least check a couple things before settling down on a bar plot.

It's worth mentioning that I was inspired by many researchers who have tweeted on the limitation of bar graphs. Here is a publication: Weissgerber et al., 2015, PLOS Biology.

2\. Friends Don't Let Friends Make Violin Plots for Small Sample Sizes
======================================================================

This is quite common in the literature as well, but unfortunately, violin plots (or any sort of smoothed distribution curves) make no sense for small n.

Distributions and quartiles can vary widely with small n, even if the underlying observations are similar. Distribution and quartiles are only meaningful with large n. I did an experiment before, where I sampled the _same_ normal distribution several times and computed the quartiles for each sample. The quartiles only stablize when n gets larger than 50.

3\. Friends Don't Let Friends Use Bidirectional Color Scales for Unidirectional Data
====================================================================================

Excuse my language, but this is a truly data visualization sin, and again quite common. I can understand why this error is common, because it appears that many of us have not spent a lot of thoughts on this issue.

Color scales are pretty, but we have to be extra careful. When color scales (or color gradients) are used to represent numerical data, the darkest and lightest colors should have special meanings. You can decide what those special meanings are: e.g., max, min, mean, zero. But they should represent something meaningful. A data visualization sin for heat maps/color gradients is when the lightest or darkest colors are some arbitrary numbers. _This is as bad as the longest bar in a bar chart not being the largest value._ Can you imagine that?

4\. Friends Don't Let Friends Make Bar Plot Meadow
==================================================

We talked about no bar charts for mean separation, but this is a different issue. It has to do with presenting results of a multi-factorial experiment. Bar plot meadows are very common in scientific publications and unfortunately also _ineffective_ in communicating the results.

Data from: Matand et al., 2020, BMC Plant Biology

Bar plot meadows are common because multi-factorial experiments are common. However, a bar plot meadow is poorly designed for its purpose. To communicate results of a multi-factorial experiment, it requires thoughtful designs regarding grouping/faceting by factors of interest.

In this example, I focus on comparing the effect of `Treatment` & `Explant` on `Response` at the level of each `Variety`. However, if the focus is the effect of `Treatment` & `Variety` on `Response` at the level of each `Exaplant`, then it will require a different layout.

5\. Friends Don't Let Friends Make Heatmap without (Considering) Reordering Rows & Columns
==========================================================================================

Heatmaps are very common in scientific publications, and _very very_ common in omics papers. However, for heatmaps to be effective, we have to consider the ordering of rows & columns.

In this example, I have cells as columns and features as rows. Grids are showing z scores. It is impossible to get anything useful out of the heatmap without reordering rows and columns. We can reorder rows and columns using clustering, but that is not the only way. Of course, if the rows and columns are mapping to physical entities (rows and columns of a 96-well plate), then you can't reorder them. But it is a very good idea to at least consider reordering rows and columns.

Data from: Li et al., 2022, BioRxiv

Bonus: heatmaps can be very pretty
----------------------------------

...if you are good are reordering rows/columns and choosing color gradients. Here is an example "abstract aRt" generated from simulated data.

R code for this aRt piece can be found here.

For a tutorial on how to reorder rows and columns of a heatmap, see this markdown file.

6\. Friends Don't Let Friends Make Heatmap without Checking Outliers
====================================================================

Outliers in heatmap can really change how we perceive and interpret the visualization. This generalizes to all sort of visualizations that use colors to represent numeric data. Let me show you an example:

In this example, I have 2 observations. For each observations, I measured 20 features. Without checking for outliers, it may appear that the 2 observations are overall similar, except at 2 features. However, after maxing out the color scale around 95th percentile of the data, it reveals that the two observations are distinct across all features.

7\. Friends Don't Let Friends Forget to Check Data Range at Each Factor Level
=============================================================================

This is a common issue that many of us have encountered. In a multifactor experiment, sometimes the range of the response variable changes widely between different factor levels.

This hypothetical experiment measured 3 compounds across 2 groups (control vs. treatment). Without checking data range for each compound, you will likely have missed that the treatment had a strong effect on compound 1. This is because the concentration of compound 1 has a much narrower range than the other compounds in this experiment.

8\. Friends Don't Let Friends Make Network Graphs without Trying Different Layouts
==================================================================================

Network graphs are common in scientific publications. They are super useful in presenting relationship data. However, the appearance (not the topology) of the network can make a huge difference in determining if a network graph is effective.

Layouts can drastically change the appearance of networks, making them easier or harder to interpret. Here are 3 network graphs from the same data. They look very different from each other. Data from: Li et al., 2022, BioRxiv

Here is 9 different layouts for the _same_ network. They can look very different.

The R script to make this animation is available here

9\. Friends Don't Let Friends Confuse Position-based Visualizations with Length-based Visualizations
====================================================================================================

This is always the elephant in the room and the essence of many misleading visualizations. In this example, I measured a response variable across 3 time points. Two of the following graphs are fine, but one of them is a data visualization crime. Can you see why?

In dot and line plots, values are represented by positions along the x and y axis. The same idea applies to other position based visualizations, such as box plots. In bar plots, values are represented by the distance from the x axis, and thus the length of the bar.

The 3rd graph is not 0-based, which makes the bar length at time point 2 about 3x longer than that at time point 1. In fact, the true difference in means is closer to 1.6x. I hope you can see how confusing length and position based visualizations can lead to misleading graphs.

Watch out for bar plots with broken axis
----------------------------------------

Broken axis may be useful for depicting data across a wide range of numeric values. (Alternatively, log scaled axis can be used instead.) Broken axis are fine for position based graphics, because the data are represented by positions along the axis. However, we must be very careful with bar plots that have broken axis. Here is an example.

In this example, two graphs (left vs. right) are showing the same data. However, by changing where the axis is broken, one can make certain bars looks longer or shorter. In this example, the length of bar "d" can look _really_ different. The illusion of bar "d" being very short on the right graph boils down to bar plot being a length based graphics, not a position based graphics.

Example R code for broken axis can be found here.

10\. Friends Don't Let Friends Make Pie Chart
=============================================

Pie chart is a common type of visualization for fractional data, where fractions add up to 100%. This is achieved by dividing a circle into sectors, and the sectors add up to a full circle. Pie charts have been criticized, because human are much worse in reading angles and area than reading lengths. Here is a blog post that explores that.

In this example, we have two groups, each contains 4 sub-categories. In classic pie charts, the angles (and thus arc lengths & sector area) represent the data. The problem is that it is _very_ difficult to compare between groups. We can visually simplify the pie chart into donut charts, where the data are now represented by arc lengths. However, if we want to use lengths to represent the data, why don't we just unwrap the donut and make stacked bars? In stacked bar graphs, bars are shown side-by-side and thus easier to compare across groups.

Fun fact: the scripts underlying stacked bars are much simpler than those underlying the pie charts and donut charts. If you want to produce sub-optimal graph types with ggplot, you actually have to work extra hard.

11\. Friends Don't Let Friends Make Concentric Donuts
=====================================================

In this example, we have 3 groups, each of which contains two sub-categories (Type I or Type II).

In concentric donuts, you might be tempted to say the data are represented by the arc lengths, which is in fact **inaccurate**. The arc lengths on the outer rings are much longer than those in the inner rings. Group 2 and Group 3 have the same exact values, but the arc lengths of Group 3 are much longer. In fact the data are represented by the _arc angles_, which we are bad at reading.

Since outer rings are longer, the ordering of the groups (which group goes to which ring) has a big impact on the impression of the plot. It can lead to the apparent paradox where larger values have shorter arcs. The better (and simpler!) alternative is just unwrap the donuts and make a good old stacked bar plot. BTW, this is also my main issue with circos plots and other circular plot layouts.

12\. Friends Don't Let Friends Use Red/Green and Rainbow color scales
=====================================================================

Deuteranomaly is the most common type of red/green colorblindness, occurring in 1/16 male and 1/256 female. Any color scales that use shades of red and shades of green in the same time would be a problem for a person with red/green colorblindness (third column of the figure). In addition, red/green and rainbow do not preserve information well at all when printed on black/white (grey scale, second column in figure). Many scientific software still use red/green or rainbow as the default color scales, which drives me crazy. More "modern" color scales, such as viridis are both colorblind-friendly and grey scale-safe (third row of figure). And they look nice too.

13\. Friends Don't Let Friends Forget to Reorder Stacked Bar Plot
=================================================================

Stacked bar plots are useful for visualizing proportion data. Stacked bar plots are commonly used to visualize community structure or population structure or admixture analysis. This kind of visualization boils down to a collection of samples, where each sample contains multiple classes of members. However, when we have many samples and many classes, stacked bar plots need to be optimized to be effective. And by "optimize" I mean the grouping and ordering of samples.

Here we have an example data with 100 samples and 8 classes of member. Due to the number of samples and classes, it is very hard to discern anything from this graph without optimizing the order of bars. What the heck am I looking at? After reordering the bars, **wow**, that really made a difference, don't you think? For a tutorial on how to optimize a stack bar plot, see this script.

14\. Friends Don't Let Friends Mix Stacked Bars and Mean separation
===================================================================

Sometimes a visualization gets confusing and ineffective when it tries to too many things at once. One such example is mixing stacked bar plots and mean separation plots. One displays proportional data adding up to 100%, the other displays the difference in means and dispersion around means. These are very distinct tasks in data visualization.

In this hypothetical experiment, we had blueberry plants assigned to two groups. One group was the control; the other was treated with a chemical to make fruit development faster.  
Each group had 5 plants. The response of the treatment was divided into 3 categories: light green fruits, light blue fruits, and dark blue fruits. 100 fruits from each plant were examined and the number of fruits in each category was counted. The percentage of fruits in each category was calculated and reported. The question of the study is: did the chemical treatment work?

The first stacked bar plot is fine as the standard way to visualize proportion data. It is clear that all categories add up to 100%, and the chemical treatment strongly shifted the color profile towards the most developed stage (dark blue).

The middle stacked bar plot is problematic, mainly because it is trying to do two distinct data visualization tasks at once. When error bars and dots are overlaid onto the stacked bars, it become unclear which error bars and dots are being compared. Due to the nature of stacked bars, the error bars and dots of the upper stacks have to be shifted upwards, and thus interpretation of the y-axis for error bars and dots become not straightforward.

Finally, if the main point of the visualization is mean separation and dispersion around the mean, the third graph is the better choice. There is no ambiguity on which comparisons are being made. As shown in the first stacked bar plot, the chemical treatment strongly increases the proportion of dark blue fruits, at the expense of lighter color fruits.

Conclusion (?)
==============

That's it for now. I will update this when I have the time (and inspirations) to produce more examples. Not sure what the next one will be, but stay tuned!
