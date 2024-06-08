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
```
Extendible Hashing:
To avoid that a duration of hash table rebuilding takes too long, we decompose it into small pieces. 
```

1. Directory
	```
	Directory depth d: number of bits of the index of the hash table
	```
	1. according to the hash value, just checking for directory depth, insert to the correct box.
	2. if the box overflow, ask need to add bit? if yes, **increase d** until collision is resolved.
	3. reallocate the nubmers in the bucket overflow to their new correct bucket according to the new depth.
	4. only the directory that it's bucket  already has been inserted should switch the arrow to its bucket .
	

2. Directoryless
	don't wnat to use the whole hash table, so utilize *r* & *q* to control the usage area.
	→ the area is $[0, 2^r+q-1]$
	
	**when collision:**
	1. open new bucket: number $2^r+q$
	2. rearange the numbers in the *q* bucket by $h(k, r+1)$ (they'll be put into $q$ or $2^r+q$)
	3. $q = q+1$;  if $q=2^r$, then $q=0$ and $r = r+1$.
	**every time insert:**
	1. check $h(k, r)$
	2. if $h(k,r)<q$, then check $h(k, r+1)$
	3. insert, and check **if collision happens**.

**comparison**

|                       | directory | directoryless |
| --------------------- | --------- | ------------- |
| when collision        | *2        | +1            |
| resolve the collision | always    | maybe         |







