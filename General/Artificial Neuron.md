What does an artificial neuron do?

- Takes an input
- Processes it
- Sends it through an activation function
- Return the activated output

Computes some function *f* of the weighted sum of its inputs

$$ y_i = f(\sum_{j} w_{ij}y_j)$$

$w_i$ is the weight applied to some input $y$. As far as I'm aware, $y_i$ can be some type of constant or function

![](https://cnl.salk.edu/~schraudo/teach/NNcourse/figs/unit.gif)


This sum $\sum_{j} w_{ij}y_j$ is called the net input to unit *i*. This is written as $net_i$

*f* is known as the **activation function** of the unit. 

What does this mean? There are some amount nodes $y_i$ that exists. Their importance is weighted with some weight $w_i$. This weight determines the strength of the node in making a decision. The chained results of the nodes (denotated by the sum of the nodes) is then put through an **activation function** $f$. 