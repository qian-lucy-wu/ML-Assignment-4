# Assignment 4: Double Logistic Regression, Bootstrapping, RDD, and KNN

Language: Python

Due: Sunday, February 12th 11:59 PM

 

Please submit your writeup and code in one Python notebook.

Provide evidence to support your answers. 

 

Answer the following questions:

1. Using hotel_cancellation.csv, write code to estimate the treatment effects if a ‘different room is assigned’ as the treatment indicator and interpret its effect on the room being ‘canceled’. Use all the other columns as the covariates. Write your observations for the results.

2. For hotel_cancellation.csv, now use double logistic regression to measure the effect of ‘different room is assigned’ on the room being ‘canceled’..

3. Use bootstrap to estimate the standard error of the treatment effects measured in (2).

As we discussed in class, a regression discontinuity design (RDD) is a quasi-experimental design that aims to determine the causal effects of interventions by studying observations close to a threshold above or below which an intervention is assigned (the example I used in class was “imagine college assignment only depended on your SAT score and the cutoff was 800 points to get into college”). By comparing observations lying closely on either side of the threshold, it is possible to estimate the marginal treatment effect in environments in which randomization is unfeasible (in the college example, one would compare the outcomes of all the people at score 800 to those at score 799).

4. Use the drinking.csv for this question. Keeping 21 as the threshold for age, explore the data with an RDD by writing very simple code (no package needed, just average to one side of the threshold minus average to the other side) to determine if alcohol increases the chances of death by accident, suicide and/or others (the three given columns) and comment on the question “Should the legal age for drinking be reduced from 21?” based on the results. Plot graphs to show the discontinuity (if any) and to show results for the change in chances of death with all the three features (i.e., accident vs age, suicide vs age and others vs age). For this problem, choose the bandwidth to be 1 year (i.e., 21 +- 1). What might be the effect of choosing a smaller bandwidth?  What if we chose the maximum bandwidth?

k-Nearest Neighbors (kNN) is a machine learning algorithm used for both classification and regression problems. In a kNN algorithm, data points are stored, and a prediction is made for a new data point by identifying the k nearest data points to the new data point and aggregating the results from those k data points. In a classification problem, if k = 3, the three nearest data points to the new data point are examined, and the most frequent class among those three data points is assigned as the predicted class for the new data point. In a regression problem, the mean or median value of the k nearest data points is used as the predicted output value for the new data point.

5. Use the iris.csv for this question. How does the performance of k-nearest neighbors change as k takes on the following values: 1, 3, 5, 7? Which of these is the optimal value of k? Which distance/similarity metric did you choose to use and why?
