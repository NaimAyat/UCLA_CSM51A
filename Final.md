# Final Exam Review
## Representing Logic
### Combinational Logic
* Output has no memory, solely based on current inputs
### Sequential Logic
* Output values depend both on previous inputs and state of the logic based on previous inputs
## Boolean Algebra
### Identity 
0 ^ x = 0
1 v x = 1
### Indempotence
1 ^ x = x
0 v x = x
x ^ x = x
x v x = x
### Associative
x ^ (y ^ z) = (x ^ y) ^ z
### Distributive
x ^ (y v z) = (x ^ y) v (x ^ z)
### Absorption 
x ^ (x v y) = x
x v (x ^ y) = x
### Combining
(x ^ y) v (x ^ ~y) = x
### DeMorgan's
~(x ^ y) = ~x v ~y
### Dual of a Boolean Function
* Replace ANDs with ORs
* Replace 0s with 1s and vice versa
* Example: dual of (a ^ b) v (b ^ c) is (a v b) ^ (b v c)
### Complement of a Function
~f(a, b, c, ...) = dual of f where variables are inverted
## Truth Table to Boolean Logic
### Minterm
* An expression that ANDs all the inputs of the function in direct or negated forms
* Ex. minterms of f(a, b, c) are a ^ b ^ c, ~a ^ b ^ c, ~a ^ ~b ^ c, etc.
### Maxterm
* Expression that ORs together all the inputs of a function in direct or negated forms
* Ex. maxterms of f(a, b, c) are a v b v c, ~a v b v c, ~a v ~b v c, etc.
### Relationship of Minterms and Maxterms
* A truth table row for 0000 has minterm ~d ^ ~c ^ ~b ^ ~a, and maxterm d v c v b v a
* Note that a minterm of a row equals the inverse of its maxterm

![Minterms](Images/f1.png)
### Disjunctive Normal Form
* Minterms ORed in a sum-of-products
* Fully disjunctive normal form: we ONLY OR minterms in a sum-of-products; every single term has all inputs. If it's missing an input, it is not fully
### Conjunctive Normal Form
* Maxterms ANDed in a product-of-sums
## Logic Reduction (Karnaugh Maps)
* Implicant: a product term that is true implies that the function is true
* Prime implicant: aan implicant that cannot be made any larger and still be an implicant
* Essential prime implicant: prime implicant that is the only containing a particular minterm
1. Generate K-map in order 00, 01, 11, 10
2. Group all adjacent 1s without including 0s
   * Each group (prime implicant) must be rectangular and a size that is a power of 2
3. An essential prime implicant contains at least 1 minterm not included in any other groups
4. Sum all essential groups to obtain a minimum sum of products
