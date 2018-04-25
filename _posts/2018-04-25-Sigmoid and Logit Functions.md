
I was trying to find the link between the Sigmoid (or Logistic function) and the Logit function. Surprisingly, in the limited search that I did, I could not find any derivation for the relation between the two.

Sigmoid function is the inverse function of the Logit function. Here inverse indicates that:

$$f(x) = y$$
Then g(x) is the inverse function of f(x) if and only if
$$g(y) = x$$

The Logit function is the log of odds ratio. 

$$logit(p) = log(p/(1-p))$$
$$         = log(p) - log(1-p)$$
$$         = -log((1/p)-1)$$

