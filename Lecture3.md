# Lecture 3: April 9, 2018
## Boolean Algebra Simplification
* Example: ~((a ^ ~b) v ~((~c v ~d) ^ e))
  * Write as a sum of products (an OR-ing of AND-ed terms)
  * By DeMorgan's Law: ~(a ^ ~b) ^ (~c v ~d) ^ e
  * Again, using DeMorgan's: (~a v b) ^ (~c v ~d) ^ e
  * Use product of sums: (~a v b) ^ [(e ^ ~c) v (e ^ ~d)]
  * Distribute: (~a ^ e ^ ~c) v (~a ^ e ^ ~d) v (b ^ e ^ ~c) v (b ^ e ^ ~d)
