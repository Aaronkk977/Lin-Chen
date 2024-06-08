### Key Concepts in Modular Arithmetic and the Integers Modulo $n$

#### Congruence Modulo $n$

1. **Definition**:
   - For integers \( a \) and \( b \), \( a \equiv b \mod n \) means \( n \) divides \( (a - b) \).
   - \( n \) is called the modulus.

2. **Equivalence Relation**:
   - Congruence modulo \( n \) is an equivalence relation on the set of integers \( \mathbb{Z} \).

#### Integers Modulo $n(Z_n)$

1. **Equivalence Classes**:
   - \( \mathbb{Z}_n \) consists of the equivalence classes $([0], [1], ..., [n-1])$.
   - Each equivalence class contains all integers congruent to one of the representatives $( 0, 1, ..., n-1 )$.

2. **Representation**:
   - $a \equiv b \mod n$ indicates a relation.
   - \( a = b \mod n \) means \( a \) is the remainder when \( b \) is divided by \( n \).
	**Example**:
   - \( -3 \equiv 9 \mod 6 \) (relation).
   - \( -3 \neq 9 \mod 6 \); instead, \( 3 = 9 \mod 6 \) (remainder representation).

#### Arithmetic in $Z_n$

1. **Operations**:
   - All arithmetic operations (addition, subtraction, multiplication) are performed modulo \( n \).
   - Examples:
     - \( 5 + 6 \equiv 2 \mod 3 \)
     - \( 5 \times 7 \equiv 2 \mod 3 \)

2. **Polynomial Congruence**:
   - If $f(x_1, x_2, ..., x_n)$ is a polynomial with integer coefficients and $( a_j \equiv b_j mod m )$ for \( 1 \leq j \leq n \), then \( f(a_1, a_2, ..., a_n) \equiv f(b_1, b_2, ..., b_n) \mod m \).
   - Example: \( 9^9 \mod 4 \equiv (9 \mod 4)^9 \equiv 1 \mod 4 \).

#### Extended Euclidean Algorithm

1. **Goal**:
   - Given two integers \( m \) and \( n \), find integers \( m' \) and \( n' \) such that \( mm' + nn' = \gcd(m, n) \).

2. **Significance**:
   - This algorithm is known as the extended Euclidean algorithm or B\'ezout’s identity.
   - It is crucial in various applications, including cryptography and number theory.
