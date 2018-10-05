You might have come across the terms Standard Error, Standard Deviation and other such statistical terms when trying to grasp the basics of Machine learning. Ever wondered what is the difference between Standard error and deviation. Well it turns out that the Standard Error of the mean is the standard deviation of the sampling distribution of the sample means. Well that was a mouthful. 

Let's break it up into smaller chunks. Like how we attack the inner most chunk of a nested loop, here let us start by understanding sampling distribution of sample means. Assuming that, we are trying to understand the mean height of adult(> 18 years of age) men in a country - India for instance. It is not a possible task to get the height of every adult. Hence we resort to sampling. We collect the heights of a smaller representative sample of size N and find the mean of this sample. We do this sampling process many times over - lets say 1000 times, each time picking a new sample of size N and calculating the mean. We then create a frequency distribution plot of these sample means (in other words, the x-axis would be the sample mean values and the y-axis would be the frequency count of each of these sample mean values) to get the sampling distribution of the sample means. 
Do you want to guess the shape of this sampling distribution of the sample means?

Yes you got it right - it would be a normal distribution with the middle values having the highest frequency. And more interestingly, though each of these sample means would have been off from the population mean by varying margins, the mean of these sample means would almost be the population mean. The standard deviation of this frequency distribution is the Standard Error. 

Let us understand with a working example. 
Step 1: Creating a frequency distribution of numbers between 0 and 1000 generated randomly 10000 times. The resulting frequency distribution looks far from a normal distribution. 

![](/images/orig_dist.png){:class="img-responsive"}  


Then we draw samples of size 10 from this original population and calculate their mean. We repeat this process of drawing samples and calculating mean, 1000 times. The frequency distribution of these means is plotted.

The same process is repeated for samples of size 50 and the frequency distribution plotted.

![](/images/sample_dist.png){:class="img-responsive"}  

The Standard Error or the standard deviation of the sampling distribution of the sample means is 40 for the distribution of sample size 50 and 90 for the distribution of sample size 10. This is very evident in the plots - the distribution from samples of size 50 is more tighter than the distribution from samples of size 10. Do pay attention to the range of values in the x-axis. 

The mean of the original distribution is 499 and the mean of the second distribution (of sample size 50) is also very close to 499. The mean of the first distribution (of sample size 10) is marginally different at 496.

  ```Jupyter Notebook
#Initialising variables
i = np.array ([[0.05,0.1]]) # Single record input array
o = np.array ([[1]]) # Output for the Single training example
output_neurons = 1
hidden_neurons = 2
wh= np.array ([[0.15,0.25],[0.2,0.3]]) # 2 x 2  matrix  - number of input features x number of hidden nodes
wout=np.array([[0.40],[0.45]]) # 2  x 1 - number of hidden nodes x number of output nodes
```



