The Heaviside step function is defined as

$$
H[n]=
\begin{cases}
0, n \leq 0\\
1, n > 1
\end{cases}
$$

![](https://www.intmath.com/laplace-transformation/svg/svgphp-unit-step-functions-definition-1a-s0.svg)

How does this affect the neuron?

First let's define some "fire" threshold T. The result of the activation function is then

$$ A(x) = 
\begin{cases}
    1, Y > T\\
    0, Y <T
\end{cases}$$

Where 1 represents *fire* and 0 represents *don't fire*

What this allows you to do is classify a result as "Yes" or "No".

Pros:
* It's simple to use. It's a "Yes" or a "No" - Either fully activated or not 
* Allows less wiggle room on activations - learning becomes smoother and easier


Cons:

* Hard to chain these types of neurons. If one neuron in the chain is activated, then all will be activated.
* No variability in how "activated" the neuron is. Either it's 100% activated or 0% activated. This doesn't allow for fluent systems.