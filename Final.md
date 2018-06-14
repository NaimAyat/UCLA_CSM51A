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
