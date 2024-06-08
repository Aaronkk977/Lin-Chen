1. **To prove that a loop-free undirected graph G=(V,E)G = (V, E)G=(V,E) is bipartite if and only if χ(G)=2**
	
	we need to show two implications:
	2. If GGG is bipartite, then χ(G)=2\chi(G) = 2χ(G)=2.
	3. If χ(G)=2\chi(G) = 2χ(G)=2, then GGG is bipartite.
	
	### Implication 1: If GGG is bipartite, then χ(G)=2\chi(G) = 2χ(G)=2
	
	A graph GGG is bipartite if and only if its vertex set VVV can be partitioned into two disjoint sets V1V_1V1​ and V2V_2V2​ such that no two vertices within the same set are adjacent. In other words, every edge in GGG has one endpoint in V1V_1V1​ and the other in V2V_2V2​.
	
	**Proof:**
	
	1. Suppose GGG is bipartite. Then, by definition, there exist sets V1V_1V1​ and V2V_2V2​ such that V1∪V2=VV_1 \cup V_2 = VV1​∪V2​=V and V1∩V2=∅V_1 \cap V_2 = \emptysetV1​∩V2​=∅.
	2. Assign one color to all vertices in V1V_1V1​ and another color to all vertices in V2V_2V2​. Since there are only two colors, this is a proper coloring if no adjacent vertices share the same color.
	3. By the definition of bipartiteness, no vertices within V1V_1V1​ are adjacent to each other, and no vertices within V2V_2V2​ are adjacent to each other. Thus, this two-coloring is valid.
	4. Therefore, χ(G)=2\chi(G) = 2χ(G)=2, which means the chromatic number of GGG is 2.
	
	### Implication 2: If χ(G)=2\chi(G) = 2χ(G)=2, then GGG is bipartite
	
	If the chromatic number of GGG is 2, it means that the vertices of GGG can be colored using two colors such that no two adjacent vertices have the same color.
	
	**Proof:**
	
	1. Suppose χ(G)=2\chi(G) = 2χ(G)=2. Then there exists a proper coloring of GGG using two colors, say color 1 and color 2.
	2. Let V1V_1V1​ be the set of vertices colored with color 1, and V2V_2V2​ be the set of vertices colored with color 2. Clearly, V1∪V2=VV_1 \cup V_2 = VV1​∪V2​=V and V1∩V2=∅V_1 \cap V_2 = \emptysetV1​∩V2​=∅.
	3. Since this is a proper coloring, no two adjacent vertices share the same color. Therefore, all edges in GGG must have one endpoint in V1V_1V1​ and the other in V2V_2V2​.
	4. By definition, this means GGG is bipartite.
	
	### Conclusion
	
	Combining both implications, we have shown that GGG is bipartite if and only if χ(G)=2\chi(G) = 2χ(G)=2. Thus, we have proven the equivalence.
	
1. **Prove: Trees are planar.** 
	• A tree contains no cycles. 
	• So it cannot contain a subgraph homeomorphic to K3,3 or K5. 
	• according to Kuratowski’s theorem, trees are not planar.
	
1. **The Unity is Unique**
	
	Let (R,+,⋅)(R, +, \cdot)(R,+,⋅) be a ring with unity, and let 111 and 1′1'1′ be two unities in RRR. We need to show that 1=1′1 = 1'1=1′.
	
	**Proof:**
	1. By definition of unity, for any $a \in R$, 1⋅a=aand1′⋅a=a.1 \cdot a = a \quad \text{and} \quad 1' \cdot a = a.1⋅a=aand1′⋅a=a.
	2. In particular, this must hold when a=1′a = 1'a=1′: 1⋅1′=1′.1 \cdot 1' = 1'.1⋅1′=1′.
	3. Similarly, since 1′1'1′ is a unity, we have: 1′⋅1=1.1' \cdot 1 = 1.1′⋅1=1.
	4. Therefore, 1⋅1′=1′and1′⋅1=1.1 \cdot 1' = 1' \quad \text{and} \quad 1' \cdot 1 = 1.1⋅1′=1′and1′⋅1=1.
	5. By associativity of the ring multiplication, we know that: 1⋅1′=1′and1′⋅1=1.1 \cdot 1' = 1' \quad \text{and} \quad 1' \cdot 1 = 1.1⋅1′=1′and1′⋅1=1.
	6. Thus, 1=1′.1 = 1'.1=1′. 
1. Let f and h be permutations of S = {1,2,...n}. Then f and h are conjugate, or f~h where ~ denotes the relation, if there exists a permutation g such that g~f~g = h. Prove that conjugacy is an equivalence relation. (You need to verify the property of reflexivity, symmetry, and transitivity.)
	### Reflexivity
	
	A relation ∼\sim∼ is reflexive if every element is related to itself. We need to show that any permutation fff is conjugate to itself.
	
	Let fff be a permutation. We need to find a permutation ggg such that g−1fg=fg^{-1}fg = fg−1fg=f.
	
	We can simply choose ggg to be the identity permutation III (where I(x)=xI(x) = xI(x)=x for all x∈Sx \in Sx∈S). Then,
	
	I−1fI=fI^{-1} f I = fI−1fI=f
	
	Since the identity permutation does not change fff, this shows that f∼ff \sim ff∼f. Hence, the conjugacy relation is reflexive.
	
	### Symmetry
	
	A relation ∼\sim∼ is symmetric if f∼hf \sim hf∼h implies h∼fh \sim fh∼f. We need to show that if fff is conjugate to hhh, then hhh is conjugate to fff.
	
	Assume f∼hf \sim hf∼h. By definition, this means there exists a permutation ggg such that:
	
	g−1fg=hg^{-1} f g = hg−1fg=h
	
	To show that h∼fh \sim fh∼f, we need to find a permutation g′g'g′ such that:
	
	g′−1hg′=fg'^{-1} h g' = fg′−1hg′=f
	
	Let's choose g′=g−1g' = g^{-1}g′=g−1. Then,
	
	g′−1hg′=(g−1)−1hg−1=ghg−1g'^{-1} h g' = (g^{-1})^{-1} h g^{-1} = g h g^{-1}g′−1hg′=(g−1)−1hg−1=ghg−1
	
	Using the given g−1fg=hg^{-1} f g = hg−1fg=h, we get:
	
	ghg−1=fg h g^{-1} = fghg−1=f
	
	Therefore,
	
	(g−1)−1hg−1=f(g^{-1})^{-1} h g^{-1} = f(g−1)−1hg−1=f
	
	This shows that h∼fh \sim fh∼f. Hence, the conjugacy relation is symmetric.
	
	### Transitivity
	
	A relation ∼\sim∼ is transitive if f∼hf \sim hf∼h and h∼kh \sim kh∼k imply f∼kf \sim kf∼k. We need to show that if fff is conjugate to hhh, and hhh is conjugate to kkk, then fff is conjugate to kkk.
	
	Assume f∼hf \sim hf∼h and h∼kh \sim kh∼k. By definition, this means there exist permutations g1g_1g1​ and g2g_2g2​ such that:
	
	g1−1fg1=hg_1^{-1} f g_1 = hg1−1​fg1​=h g2−1hg2=kg_2^{-1} h g_2 = kg2−1​hg2​=k
	
	We need to find a permutation ggg such that:
	
	g−1fg=kg^{-1} f g = kg−1fg=k
	
	Let's choose g=g2g1g = g_2 g_1g=g2​g1​. Then,
	
	g−1fg=(g2g1)−1f(g2g1)g^{-1} f g = (g_2 g_1)^{-1} f (g_2 g_1)g−1fg=(g2​g1​)−1f(g2​g1​)
	
	Using the property of inverses, (g2g1)−1=g1−1g2−1(g_2 g_1)^{-1} = g_1^{-1} g_2^{-1}(g2​g1​)−1=g1−1​g2−1​, we get:
	
	g−1fg=g1−1g2−1fg2g1g^{-1} f g = g_1^{-1} g_2^{-1} f g_2 g_1g−1fg=g1−1​g2−1​fg2​g1​
	
	Substitute g1−1fg1=hg_1^{-1} f g_1 = hg1−1​fg1​=h:
	
	g1−1g2−1fg2g1=g1−1hg2=g1−1(g2−1hg2)g1=g1−1kg1=kg_1^{-1} g_2^{-1} f g_2 g_1 = g_1^{-1} h g_2 = g_1^{-1} (g_2^{-1} h g_2) g_1 = g_1^{-1} k g_1 = kg1−1​g2−1​fg2​g1​=g1−1​hg2​=g1−1​(g2−1​hg2​)g1​=g1−1​kg1​=k
	
	Thus,
	
	g2g1g_2 g_1g2​g1​
	
	So g−1fg=kg^{-1} f g = kg−1fg=k, meaning f∼kf \sim kf∼k.
	
	Therefore, the conjugacy relation is transitive.
3. ![[Pasted image 20240606132138.png]]