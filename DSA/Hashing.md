The biggest advantage of hashing is its high performance: O(1) time complexity.
However, it cannot always remain this efficiency as:

(1) *collision* happens or,
(2) *load factor* $\alpha$ is near or even much larger than $1$.

--------------------------------------------------------------------------
#### Two methods to deal with **collision**:

1. **open addressing**
	1. linear probing: causes *primary clustering
	2. quadratic probing: cause *secondary clustering
	3. double hashing: *uniform hasing*!
2. **chaining**
		can apply balanced BST to improve (worst case $O(nlogn)$)
		ensure $n = O(m)$ → the overall time complexity is $O(1)$.

--------------------------------------------------------------------------
#### Hash Function

--------------------------------------------------------------------------
#### Dymanic Hashing

1. Directory
2. Directoryless
