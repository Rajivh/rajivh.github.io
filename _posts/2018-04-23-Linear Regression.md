Linear Regression can be seen as a way of expressing a linear relationship between two variables (at the simplest level). Now what is a linear relationship - if the relationship between the two variables can be expressed as a straight line, then this qualifies to be a linear relationship. 

Why is this useful - let us consider an example of relation between age and income. We are interested to know if there is a strong relationship between these two variables. The strength of this relationship helps us in being able to predict the variables of interest (income) given a certain set of values of the independent variable (age).

The straight line or linear relationship between the two variables can be expressed in the form:

$$Income = Beta0 + Beta1*Age$$

Here Beta0 is the y-intercept and Beta1 is the slope of the line expressing the relationship between the two variables.

Assuming, we have multiple data points denoting Age and Income, and we plot in the xy space to get a scatter plot. 

![Plot](/images/Scatterplot.png){:class="img-responsive"}

Clearly, the two variables Age and Income follow a linear relationship.

If we get a new data point on Age and interested to find/ predict the Income for this new data point, it would help if we have a line which 'fits' the existing points - so that we can map the Age on to the line to get the corresponding Income value.

Fitting the line - One way to fit a line is by minimising the distance of all the points from this line. The distance between the line and the point(s) can be termed as the error or residual. We could have points above and below the line - thereby resulting in positive and negative errors. A simple average of such errors can be misleading as a high positive error (point above the line) can be neutralised by a high negative error (point below the line). Hence, the squares of these distances are considered and then added.

But it would be lot of work to find out the best fitting line with the least squared errors among all the possibilities - by just changing the slope and intercept.

One approach to this problem is using an algorithm called gradient descent. Before, we get into the algorithm, let us understand a couple of functions - the hypothesis function and the cost function.

The hypothesis function is our straight line equation - we hypothesize that we can fit a straight line to best describe the relationship between the Age and Income variables.

$H(x) = Beta0 + Beta1 * Age$

We would like our hypothesis function H(x) to be as close as possible to the actual Income value (y). We can achieve this by playing around with the values of Beta0 and Beta1.

For this, we define a Cost function - which is the squared distance of the errors. The error can be defined as H(x)-y. Summing the square of this error over all data points, we get,

$Cost Function J(Beta0, Beta1) = sigma i=1ton (H(xi) - yi)^2$

We need to find that particular combination of Beta0 and Beta1 that finds the minima of this Cost function.

 $|\psi\rangle$, $x'$, $x^\*$.


