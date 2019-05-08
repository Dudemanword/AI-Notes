Most commonly used activation function in deep learning models. It is defined as:

$$ f(x) = 
\begin{cases} 
0, x \leq 0\\
x, x > 0
\end{cases}
$$

![](https://i.imgur.com/gKA4kA9.jpg)

Captures **Interactions** and **Non-linearities**

Interactions are when a variable affect the outcome of another variable.

For example, if my model wanted to know whether a certain body weight indicated an increased risk of diabetes, it would have to know an individual's height. Some bodyweights indicate elevated risks for short people, while indicating good health for tall people. So, the effect of body weight on diabetes risk depends on height, and we would say that weight and height have an interaction effect. 

(https://www.kaggle.com/dansbecker/rectified-linear-units-relu-in-deep-learning)


Non-Linearities are when your predictions vs outcome don't fit on a linear line in a Cartesian plane (The effect of increasing the predictor by one is different at different values of that predictor)


How does it capture interactions?

Take a node $f(2a + 3b)$. The output of the node when put through a ReLu activation function is as follows:

$$f(2a + 3b) =
\begin{cases}
2a + 3b, a > 0, b > 0\\
2a + 3b, b > \frac{2}{3}a \, b > 0\\
2a + 3b, a > \frac{3}{2}b \, a > 0\\
0, a < 0 \, b < 0\\
etc.
\end{cases}$$

From the result mappings, it's clear that relationship between $a$ and $b$ change the result of the node

Non linearities are captured through a **bias** that gets attached to the output. ie $f(2a + 3b + \delta)$ where $\delta$ represents the bias. In a many noded project, the bias gets attached per node which allows for a range of slopes for the output.

