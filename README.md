# Solving Graph Coloring problem with Grovers Algorithm

Graph coloring problem or more precisely proper vertex coloring problem is defined as: Given a graph and a set of k labels, we have to assign labels to the vertices such that  vertices which are connected do not have the same label. This problem can be used to effectively model situations like scheduling problem, register allocation problem and so on.

For graphs with only few vertices(nodes), estimating the minimum number of colors (labels) and assigning them is a fairly simple procedure. But for large number of nodes, the problem becomes much more difficult. The code in this repository corresponds to the solving the problem of allocating labels to the fully connected rectangle + an extra connected node(five vertices and seven edges), using Qiskit. 
![rsz_general](https://user-images.githubusercontent.com/70852403/216637255-b79397e1-6493-4fa6-9ab4-4acde058a37e.png)


Unlike classical algorithms, the Grover's search algorithm have an optimal iteration number at which the probability to correctly measure the 
desired states is the highest. If there are $N$ possible solutions and out of them, if $M$ of them are solution states, we can approximate the
number of iterations "I" by,
```math
     I = \frac{\pi}{4} \sqrt{\frac{N}{M}}
```
In the 5 vertex graph, we have $N$= 4x4x4x4x4 = 1024 states, and. $M$=4x3x2x1x3 = 72 states, which gives the optimal number of iterations = 3.

We need atleast 4 colors for this graph. For each node, 2 qubits are assigned and after the computation, the results are further processed(specific details can be found as comments in the code) and the graph with corresponding node colors are drawn using the networkx python package for easy visualisation. The results are given below.

Qiskit Ouput:

![qis](https://user-images.githubusercontent.com/70852403/216637714-c757923a-4f36-43bf-bfa7-4d3182c2d0a7.png)

Corresponding colored graphs:

![rsz_0011100110 (1)](https://user-images.githubusercontent.com/70852403/216638330-edc998bc-5039-4e6e-a43b-d4f68fbec56d.png)

![rsz_1001110011](https://user-images.githubusercontent.com/70852403/216638522-5f1ece62-b189-4ff1-a52b-472c3dd21a7b.png)

