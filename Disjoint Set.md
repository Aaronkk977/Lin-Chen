### 1. equivalence relation
1. reflexive
2. symmetric
3. transitive
if we distribute every element in S to different *quivalence class*, then every element would only belong to unique one *quivalence class*. → if every two set has no intersection, then they are ***disjoint set***.

### 2. Operations
1. **MAKE-SET**
3. **FIND-SET**
4. **UNION**
		if  FIND-SET(A) $!=$ FIND-SET(B)  UNION(A,B)
		
Below are some implements:
##### 2.1 Array 法
index → element's ID
value → set ID to which the element belongs

##### 2.2 Tree - array 法
index → element's ID
value → set ID to which the element belongs(root) or ***it's parent***(other nodes).

→ ***Union by Height*** 
→ ***Path Compression***
![[Pasted image 20240603224720.png]]
##### 2.3 Linked-list
(SKIP)

ALL of ABOVE can use weighted union to faster.

### 3. Amortized Analysis
![[Pasted image 20240603223239.png]]
