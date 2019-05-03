$$A = cx$$

Activation of the neuron is proportional to input

Pros

* Allows for a range of activations. This allows chaining of neurons (take the max of the neurons)

* Because $A'$ is constant (slope = _c_), the error from the calculation is also constant (Can also be a con) 

Cons

* Only allows for operation on simple data.
* Less range to actually map resultant data

It's bad to chain linear layers. Take some neurons $y_1, y_2, y_3$ with some activation functions 

$$A(y_1) = c_1y_1 
\newline 
A(y_2) = c_2y_2
\newline
A(y_3) = c_3y_3$$ 

Now chain the neurons together in the order $y_1 \rightarrow y_2 \rightarrow y_3$ such that the results of each of the activation functions feed into each other:

$$
A_{y_1y_2}(x) = A_{y_2} \circ A_{y_1}
\newline
A_{y_1y_2}(x) = c_2c_1y_1
\newline
A_{y_1y_2y_3} = A_{y_1y_2} \circ A_{y_3}
\newline
$$

which produces the result

$$
A_{y_1y_2y_3}(x) = c_3c_2c_1y_1
$$

The important conclusion here is that **The end result is only dependent on the result of the first neuron**

