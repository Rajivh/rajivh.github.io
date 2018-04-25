
I was trying to find the link between the Sigmoid (or Logistic function) and the Logit function. Surprisingly, in the limited search that I did, I could not find any derivation for the relation between the two.

Sigmoid function is the inverse function of the Logit function. Here inverse indicates that:

$$f(x) = y$$
Then g(x) is the inverse function of f(x) if and only if
$$g(y) = x$$

The Logit function is the log of odds ratio. 

$$logit(p) = log(p/(1-p))$$
$$         = log(p) - log(1-p)$$
$$         = -log((1/p)-1)$$

The Sigmoid function is given by
$$1/(1+e^{-x})$$

Now substituting x with the logit function output, we get
$$1/(1+e^{-(-log((1/p)-1)})\\=1/(1+(1/e^{-log((1/p)-1)}))\\$$

Substituting, ((1/p)-1) to be x,

$$e^{-log(x)}/(1+e^{-log(x)})$$
$$\\$$
$$=e^{log(x)^{-1}}/(1+e^{log(x)^{-1}})$$
$$\\$$
$$=x^{-1}/(1+x^{-1})\\$$
$$=(1/x)/(1+(1/x))\\$$
$$=1/(x+1)\\$$
$$=1/((1/p)-1+1)\\$$
$$=p$$

Thus, we understand that Sigmoid function is the inverse of Logit function.

While the logit function has values ranging from 
$$-infinity to +infinity$$

the sigmoid function has values ranging from 0 to 1.
