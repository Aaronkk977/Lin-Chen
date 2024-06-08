A group is a mathematical structure consisting of a set $G$ and a binary operation $\circ$ that combines any two elements of the set to form another element within the same set. 

### Properties must be met to qualify as a group:
1. **Closure**: For any two elements $a$, $b$ in $G$, the result of the operation $a \circ b$ is also in $G$.
2. **Associativity**: For any three elements $a$, $b$, and $c$ in $G$, the operation satisfies $a \circ (b \circ c)$ = $(a \circ b) \circ c$.
3. **Identity Element**: There exists an element $e$ in \( G \) such that for every element \( a \) in \( G \), the equation $a \circ e = e \circ a = a$ holds.
4. **Inverse Element**: For each element $a$ in $G$, there exists an element $b$ in $G$ such that $a \circ b = b \circ a = e$, where $e$ is the identity element.

	Addition: **abelian**(**commutative** )
	- For any two elements $a$ and $b$ in $G$, the equation $a \circ b = b \circ a$ holds.

**Inverses**
1. $(a^{-1})^{-1} = a$
2. $(a \circ b)^{-1} = b^{-1} \circ a^{-1}$


![[Pasted image 20240605211528.png]]
#### Criterion for being a Subgroup:
Let $H$ be a nonempty subset of a group $(G, \circ)$. 
$H$ is a subgroup of $G$ ⇔ 
1. For all $a, b \in H$, $a \circ b \in H$  (closure)
2. For all $a \in H$, $a^{-1} \in H$ (inverse).
or
1. $a \circ b^{-1} \in H$, for $a, b \in H$
finite version:
Let H be a nonempty subset of a finite group (G, ◦ ). 
$H$ is a subgroup of $G$ ⇔  for all $a, b \in H$,  $a \circ b \in H$ (closure).
### Homomorphism 
Definition:
A homomorphism between two groups $(G,\circ)$ and $(H, \circ')$ is a function $f : G \to H$ that preserves the group operation. This means that for any elements $a, b \in G$, the function $f$ satisfies the following property:
$$f(a \circ b) = f(a) \circ' f(b)$$
### Conjugacy
two elements $f$ and $h$ of a group $G$ are said to be ***conjugate***. i.e. $f\sim g$ to each other if there exists an element $g$ in $G$ such that:
$$g^{-1} \circ f \circ g = h$$
Conjugacy is an ***equivalence relation*** because it satisfies:
1. **Reflexivity**: Every element is conjugate to itself.
2. **Symmetry**: If f is conjugate to h, then h is conjugate to f.
3. **Transitivity**: If f is conjugate to h and h is conjugate to k, then f is conjugate to k.