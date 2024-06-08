### 1. Basic Knowledge
##### 1.1 5 rules:
1. every node is red or black.
2. root is black.
3. every leaf is black.
4. a <mark style="background: #FF5582A6;">red</mark> node's parent or children must be <mark style="background: #CACFD9A6;">black</mark>.
5. a node's black height is path-independent.
``` 
Black Heigh
definition: 
	From current node, go down and count how many black nodes traversed.
some notes:
	1. path-independent
	2. the node itself does't count!
	3. mind that LEAF sometimes would be ignored!!!
```

##### 1.2 The prove of RE tree's height 
![[Pasted image 20240603183313.png|##xx-small]]
![[Pasted image 20240603183331.png]]
##### 1.3 Rotate
![[Pasted image 20240603183557.png]]
![[Pasted image 20240603183629.png]]

### 2. Insert & Delete
##### 2.1 Insert
1. Like insert normal BST, the new node is going to be insert to the leaf.
2. remember to add two leaf children(NIL).
3. the new node is <mark style="background: #FF5582A6;"> RED</mark>!
	⇒ if the parent is also RED, need to adjust.
**Adjustment after insert**
![[Pasted image 20240603184643.png]]![[Pasted image 20240603184656.png]]
**Code:**
```
RB-Insert-Fixup(T,z) 
While z.p.color==RED (如果你爸是紅色的) 
	if z.p==z.p.p.left (如果你爸是你爺爺左邊的小孩) 
		y=z.p.p.right (那麼叔叔就是你爺爺右邊的小孩) 
		if y.color==RED (如果叔叔是紅色的) 
			z.p.color=BLACK (就把爸爸設成黑色的) 
			y.color=BLACK (叔叔也設成黑色的) 
			z.p.p.color=RED (爺爺設成紅色的) 
			z=z.p.p (把自己變成爺爺)
		else 
			if z==z.p.right (如果你是你爸右邊的小孩) 
				z=z.p (把自己變成你爸) 
				LEFT-ROTATE(T,z) 
			z.p.color=BLACK (把你爸變成黑色) 
			z.p.p.color=RED (把你爺爺變成紅色) 
			RIGHT-ROTATE(T,z.p.p) 
	else if z.p==z.p.p.right (如果你爸是你爺爺右邊的小孩, 如前, 但left, right反過來) …… 
	
T.root.color=BLACK (最後把root改成黑色)
```
##### 2.2 Delete
If the deleted node is <mark style="background: #CACFD9A6;">BLACK</mark> and is not root, it become B+B and need adjustment.
![[Pasted image 20240603192044.png]]
**Code:**
```
RB-Delete-Fixup(T,x) 
while x!=T.root && x.color==BLACK (你不是root而且是黑的) 
	if (x==x.p.left) (你是你爸的左邊小孩) 
		w=x.p.right (你弟就是你爸右邊小孩) 
		if w.color==RED (如果你弟是紅色的) 
			w.color=BLACK (把你弟設成黑色) 
			x.p.color=RED (你爸設成紅色) 
			LEFT-ROTATE(T,x.p) 
			w=x.p.right (你新弟弟是現在你爸右邊小孩) 
		if w.left.color==BLACK && w.right.color==BLACK (兩個姪子都黑) 
			w.color=RED (把弟弟設成紅的) 
			x=x.p (你變成你爸) 
		else 
			if w.right.color==BLACK (你姪子右黑左紅) 
				w.left.color=BLACK (左邊姪子設成黑的) 
				w.color=RED (你弟設成紅的) 
				RIGHT-ROTATE(T,w) 
				w=x.p.right (新弟弟是現在你爸右邊小孩) 
			w.color=x.p.color (弟弟設成爸爸的顏色) 
			x.p.color=BLACK (爸爸設成黑的) 
			w.right.color=BLACK (右邊姪子設成黑的) 
			LEFT-ROTATE(T,x.p) 
			x=T.root (你直跳root, 準備出去) 
	else (x==x.p.right) (如果你是你爸右邊的小孩,跟前面一樣, 只是left, right都反過來) 
	
x.color=BLACK (如果跳出迴圈了, 也就是x是紅加黑, 或是root是黑加黑, 把它設成一個黑色即可)
```
