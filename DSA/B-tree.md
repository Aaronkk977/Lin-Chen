**Origin of name**：發明者從未解釋，後人推測Ｂ可能意味著Boeing(the Lab name)或Bayer(inventor's name)
## 1. Overview

**charctaristics:
* balanced
* very large "branching factor"
* Height is short (due to the large branching factor)

**advantages:
* store large amount of data ( -> use second storage -> decreasing the number of operations)
## 2. Definitions
1. ![[basic_b-tree_characteristics.png]]
3. keys in a node are non-decreasing order.
4. t：**t>=2**, degree of tree (branching factor), a node could have ***at least t*** and ***at most 2t*** ( called *full*) children.
```
Note: Root can have only 1 node and 2 children at least.
```
## 3. Operations
### a. insert

### b. delete
the outline graph of deletion:![[outline_graph_of_b-tree_deletion.png]]
```
Note: Merge child in deletion is the only way to shorten the tree. This happen when the current node is root and it has only one key.
```