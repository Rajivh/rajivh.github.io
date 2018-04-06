Notes on perceptron and neural network introduction (http://neuralnetworksanddeeplearning.com/chap1.html)

A perceptron can be thought of accepting multiple weighted inputs and producing an output with respect to a threshold. More detailed - car purchase decision (whether or not to buy a car) - multiple factors in very simple terms - adds to convenience or not , expense is manageable or not, reduces commute time or not. Now these factors can be weighted based on one’s preferences - let us assume, convenience and reduces commute time have a weight of 3 each and expense is manageable has a weight of 8. Let the threshold be 5. Now if the expense is manageable and even if the other two factors are 0, the perceptron outputs a 1 and gives a green signal for the car purchase decision. Now if the expense is not manageable, but the other two factors are 1, then also the perceptron signals a green for the car purchase decision. We could play around with the weights and the threshold to aid our decision making.


A perceptron can be in a network of layers. The perceptron in each layer supplies weighted outputs which is read by all the perceptrons in the subsequent layer. The perceptrons in the subsequent layer then apply a threshold and provide outputs which are again weighted and supplied as input to the subsequent layer and so on.


&sum; w<sub>j</sub>x<sub>j</sub> >= threshold, 1

&sum; w<sub>j</sub>x<sub>j</sub> < threshold, 0

INtroduce the concept of bias. Bias is -threshold. 

&sum; w<sub>j</sub>x<sub>j</sub> + Bias >= 0, 1

&sum; w<sub>j</sub>x<sub>j</sub> + Bias < 0, 0


So when the bias is extremely high, the perceptron will easily output 1 whereas if the bias is extremely negative, then it is difficult to get the perceptron to fire (1 output)

When it comes to more complex problems, like digit recognition, the perceptron is not ideal. Why - a small change in the weights can completely change the output from 0 to 1 - whereas what we need is gradual changes which does not disturb the other outputs. 



Example - Let us use a perceptron

h<sub>&theta;</sub>(x) = &theta;<sub>o</sub> x + &theta;<sub>1</sub>x


Introduce sigmoid neurons - sigmoid fucntion. 1/ (1 + exp(-z)). Here z is the weighted sum of the inputs along with the bias term.

z = wj.xj + Bias

