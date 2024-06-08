**The reason for calling it a "ring":** the idea of closure under addition and multiplication
**What's *closure*?** When you add or multiply elements within a ring, you stay "within" the set of elements. 
**So?** This concept can be visualized as forming a closed loop or circle of operations.

#### some fundamental rules of +
1. **commutative law :** a + b = b + a . 
2. **associative law**: a + (b + c)=(a + b) + c . 
3. **existence of the additive identity or zero element**: There exists z ∈ R such that $a + z = z + a = a$ for every a ∈ R .
4. **additive inverse**: $a + b=b + a= z$ 

#### some fundamental rules of $\cdot$
1. *no necessarily commutative*
2. **assocative law**
3. *no necessarily has the existence of multiplicative identity*:
	$a\cdot u=u\cdot a = a$ ---→ if has, it's called *a ring with unity*.
4. *no necessarily has multiplicative inverse*: 
	$a\cdot b=b\cdot a = 1$ ---→ if has, it's called *a unit*.

addition: **distributive laws of · over +**

>To determine if a set with two operations $(R, +, \cdot)$, there are **6 properties** need to varified. 

#### some BASIC FACTS
1. The *additive identity(zero element)* & *additive inverse* of a ring element are unique.
2. if (R, +, $\cdot$) be a ring with unity. (1) The unity (multiplicative identity) is unique. (2) by(1), the multiplicative inverse is also unique.
------------------------------------------------------------------
**Prove:** The Unity is Unique
	 Let (R, +, $\cdot$) be a ring with unity. The unity (multiplicative identity) is unique.
	1. Suppose \(1\) and \(1'\) are both unity elements in \(R\).
	2. By definition of a unity, for any \(a \in R\):
	   - $1 \cdot a = a \cdot 1 = a$
	   - $1' \cdot a = a \cdot 1' = a$
	3. Consider the product $1 \cdot 1'$:
	   - Since $1'$ is a unity, $1 \cdot 1' = 1$
	   - Since \(1\) is a unity, $1 \cdot 1' = 1'$
	4. Therefore, $1 = 1'$.

--------------------------------------------------------------------------
3. A unit in a ring R cannot be a proper divisor of zero.
```
proper divisor of zero: a non-zero element but can multiply another element and make the product is zero.
```

**integral domain**: if R has no proper divisor of zero.
**field**: every non-zero element is a unit.

**Theorem**: a *Field* must be a *Integral Domain*.
