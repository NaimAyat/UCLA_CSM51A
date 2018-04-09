# Lecture 3: April 9, 2018
## Boolean Algebra
### Simplification
* Example: ~((a ^ ~b) v ~((~c v ~d) ^ e))
  * Write as a sum of products (an OR-ing of AND-ed terms)
  * By De Morgan's Law: ~(a ^ ~b) ^ (~c v ~d) ^ e
  * Again, using De Morgan's: (~a v b) ^ (~c v ~d) ^ e
  * Use product of sums: (~a v b) ^ [(e ^ ~c) v (e ^ ~d)]
  * Distribute: (~a ^ e ^ ~c) v (~a ^ e ^ ~d) v (b ^ e ^ ~c) v (b ^ e ^ ~d)
## Minterms and Maxterms
* A *minterm* of a function is an expression that ANDs together all the inputs of the function in direct or negated forms
  * Denoted m(function)
  * Example: some minterms of f(a,b,c): 
    * a ^ b ^ c
    * ~a ^ b ^ c
    * ~a ^ ~b ^ c
* A *maxterm* of a function is a function that ORs together all the inputs of the function in direct or negated forms
  * Deonoted M(function)
  * Example: some maxterms of f(a,b,c): 
    * a v b v c
    * ~a v b v c
    * ~a v ~b v c
* The complement of a minterm is the respective maxterm
  * This can be verified with De Morgan's Law
## Normal forms of a Boolean Function
* Disjunctive normal form: several minterms are OR-ed in a sum of products
  * Ex: f(a,b,c) = (a ^ b ^ c) v (a ^ ~b ^ ~c) v (a ^ ~b ^ c)
* Conjunctive normal form: several maxterms are AND-ed in a product of sums
  * Ex: f(a,b,c) = (a v b v c) ^ (a v ~b v ~c) ^ (a v ~b v c)
* Example: find the dual function and write it in normal form for f(x,y) = (x ^ ~y) v (~x ^ y)
  * f<sup>D</sup> = (x v ~y) ^ (x v ~y) = (x ^ ~x) v (x ^ y) v( ~y ^ ~x) v (~y ^ y) = (x ^ y) v (~x ^ ~y)
## Karnaugh Maps
* [Visual tool for simplifying Boolean expressions](https://www.youtube.com/watch?v=A0XupfXiKIo)
