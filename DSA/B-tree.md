**Origin of name**：發明者從未解釋，maybe meaning Boeing(the Lab name) or Bayer(inventor's name)
## 1. Overview

**charctaristics:**
* balanced
* very large "branching factor"
* Height is short (due to the large branching factor)

**advantages:**
* store large amount of data ( -> use second storage -> decreasing the number of operations)
## 2. Definitions
1. ![[basic_b-tree_characteristics.png|#x-small]]
3. keys in a node are non-decreasing order.
4. **t>=2**, degree of tree (branching factor), a node could have ***at least t-1*** and ***at most 2t-1*** ( called *full*) keys.
	```Note: Root can have only 1 node and at least.```

**Terminology**:
1. $x.n$：number of keys in $x$ node.
2. $x.key_k$ : $k^{th}$ key of $x$ node.
3. $x.c_k$ : $k^{th}$ pointer to child.

## 3. Operations
### a. search
![[Pasted image 20240602194124.png|#xx-small]]
### b. insert
##### main
is root full?  if yes, split it.
is this level a leaf?  if yes, insert the key & it's the **end**.
	is the below level full? if yes, split it.

![[Pasted image 20240602202814.png|#xx-small]]

##### split
![[Pasted image 20240602195514.png]]
5~6: copy **right part** to new node.
7~9: if not leaf, copy their children's address, too.
11~15: **left shift** the keys bigger than $x.c_i.t$ in $x$ node and their children's address.
16: the ***middle key($x.c_i.t$)*** go up to $x$ node.
#### insert-nonfull
![[Pasted image 20240602202715.png]]
### c. delete
the outline graph of deletion:![[outline_graph_of_b-tree_deletion.png]]
```
Note: Merge child in deletion is the only way to shorten the tree. This happen when the current node is root and it has only one key.
```