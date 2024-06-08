### 1. Terminology

- **simple graph**: undirected, loop-free, not multigraph
- **edge**: {a, b} →  undirected ; (a, b) → digraph
- loop-free: has no self-loop
- **induce subgraph**: a subgraph that has every edges in the graph that connect with nodes in subgraph
- **connect**: start with any one node, you can go to any other node.
- <mark style="background: #FFF3A3A6;">component</mark>: maximal connected subgraph

**path**: a walk without repeated *nodes*.
**trail**: a walk without repeated *edges*.
**cycle**: a close *path*.
**circuit**: a walk *trail*.

independent set: in the set, no two nodes are adjacent.
$\alpha(G)$, ***the independence number***, the size of maximal independent set. 

#### Euler Circuits/Trials
if there is a ***circuit/trial*** that can pass through every ***edge***, then it's called Euler circuit/trial.
**Theorem**
	$G$ is an undirected graph or multigraph, and is *Euler circuit* ⇔ $G$ is ***connected*** and every node has an ***even degree***.
	$G$ is an undirected graph or multigraph, and is *Euler trial* ⇔ $G$ is ***connected*** and has exactly ***two nodes of odd degree***.
	$G$ is an digraph, and is *directed Euler circuit* ⇔ $G$ is ***connected*** and every node has ***same in degree & out degree***.

#### Handshaking Theorem
when need to solve degree-vertices-edges problem
$$\sum_{v \in V}deg(v) = 2|E|$$
#### Planar Graph
**Euler's Theorem**
$$v - e + r = 2$$

> $r$ is the number of area that the plane divided by the graph. Remind that the outer area, called infinite area, should counted.


**useful corollary**
Let $G = (V,E)$ be a connected planar simple graph with $| V | = v$ and $| E | = e > 2$. ⇒ $(3/2) r ≤ e ≤ 3v − 6$

**Kuratowski's Theorem**
statement: a graph is *non-planar*. ⇔ a graph contains a subgraph homeomorphic to $K_{3,3}$ or $K_5$.
```
homeomorphic: the graph can be rearanged without changing the connectivity of nodes.
```
#### Graph colouring
$χ(G)$
The chromatic number of the graph $G$. It is the minimum number of colors needed to color the vertices of the graph such that no two adjacent vertices share the same color.
**The four colour theorem:**
any map/graph can be coloured with just 4 colours!

**Hamiltonian cycle**
a cycle that can traverse all the vertices.





reference lecture:
[[20240425.pdf]]
[[20240509.pdf]]