# [Videos 03-08](https://www.youtube.com/playlist?list=PLSfSJnYdQad5APMQ5-S7sH2BGb60c6jGJ)
## Video 03: Boolean Algebra
### Duality Property
* Dual of a function applied to the complement of the input variables equals the complement of the function
  * f<sup>D</sup>(~a,~b,~c,...) = ~f(a,b,c)
## Video 04: Logic Gates
### Minterms
* Expression that ANDs all inputs of  function in direct or negated forms
  * Ex: there are 8 minterms for f(a,b,c): a^b^c, ~a^b^c, ~a^~b^c...
### Maxterms
* Expression that ORs all inputs of  function in direct or negated forms
### Disjunctive Normal Form
* Several minterms ORed in a sum-of-products (ORing of ANDs)
### Conjunctive Normal Form
* Several maxterms ANDed in a sum-of-products (ANDing of ORs)
## Video 05: Logic Reduction (Karnaugh Maps)
* Number of variables is an implicant is the number of literals
* Implicant is the product term that implies the function
  * 0010 v 0011 = 001X; last bit doesn't mater, we can combine minterms
### Karnaugh Map
* Represent faces of cube in square, look for adjacent minterms that differ by exactly one bit
### Definitions
* Minterm: a product term that includes each input of a logic or its compliment
* Implicant: a product term that, if true, implies the function is true. Each input to the term is a literal
  * Use theorem XY + XY' = X to form implicants
* Prime implicant: implicant that cannot be made any larger and still be an implicant
  * i.e. remainder after removing any variable is not an implicant
* Essential Prime Implicant: prime implicant that is the only one containing a particular minterm
  * A minterm that is in only one prime implicant is called *Distinguished One*
## Video 06: Hazards
### Eliminating Hazards Method 1
* Redundant implicant to cover transition
* Output no longer depends on c-transition
* Less efficient (adds a logic gate)
### Timing Problem
* Does the hazard really matter if the final logic value after the glitch is correct?
* Transitions cost power
* Transitions create noise
### Eliminating Hazards Method 2
* Use timing to remove the hazard
* Keep delay small
* Small delay makes glitch small enough to not be full transitions
### Eliminating Hazards Method 3
* Make sure delay of paths match to remove the glitch
  * cX timing is same as cN
## Video 07: Decoders and Encoders
### Combinational Building Blocks
* Decoder (binary to one-hot)
* Encoder (one-hot to binary)
* Multiplexer (select one of N)
* Arbiter (pick first of N)
### One-Hot Representation
* Represent a set of N elements with N bits
* Exactly one bit is set
* Ex: encode numbers 0 through 7
  * 000 = 00000001 = 0
  * 001 = 00000010 = 1
  * 010 = 00000100 = 2 and so on
### Decoder
* Takes binary input and converts it to one-hot
  ```
  b[i] = 1 if a = i
    b = 1<<a
  ```
### Encoder
* Inverse of a decoder
* Converts one-hot input signal to binary-encoded output signal
## Video 08: Multiplexers
* Multiplexer
  * n k-bit inputs
  * n-bit one-hot select signal s
  * Used as data selectors
  * Selects one of n k-bit inputs, s must be one-hot, `b=a[i] if s[i]===1`
### Tri-state Gates
* A gate with a control input such that if the control input is 1, then output implements the gate function, and if it is 0, the ouotput is electrically disconnected
### Logic with Muxes
* Like encoders, muxes can be used for any arbitrary logical function
* sb from a decoder is most of the AND function, the MUX performs a big OR 
#### Simplifying Mux Logic
* How can we reduce the size of the multiplexer?
  * Factor one of the sb and apply it as an input
* Approach: look at inputs to find commonalities and/or differences
#### Building Muxes out of Smaller Muxes
* Suppose you have one multiplexer with n inputs and another with m inputs
  * Can create m\*n input multiplexer
* If you have a two input mux, can build anything
  * Two input muxes can be used to create an arbitrarily large mux
  * Arbitrarily large muxes can be used to implement any logical function
