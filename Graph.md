*more terminology or math can see [[Graph Theorem]]*

<u,v> = u→v = *v is adjacent to u*
degree = in-degree + out-degree
**Connected graph** ⇔ every pair of distinct vertices u, v in V(G) is connected.
**Strongly connected**(in digraph)

##### method to express a graph
1. adjacency matrix
2. adjacency lists

**White-Path**
v is descendant of u ⇔ there is an <u>all-white path</u> from u to v at the time <u>u.d is set</u>.

##### Edges in Depth-first forest
1. **Tree edge**: 在depth-first forest裡面的邊叫tree edge. 如果v是經由(u,v) discover的, 那(u,v)就是tree edge.
2. **Back edge**: *u* → its ancestor *v*. Self-loop is also kind of back edge.
3. **Forward edge**: 連接u到它的子孫v的nontree edge (u,v). 
4. **Cross edge**: 所有其他的edge. (1) 連接同一棵depth first tree (2)連接不同depth-first tree

	**use colour of nodes to determine the type of edges**
	1. white → tree edge
	2. gray → back edge
	3. black → cross edge or forward edge (u.d<v.d → forward; u.d>v.d → cross edge)