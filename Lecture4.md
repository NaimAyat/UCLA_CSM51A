# Lecture 4: April 11, 2018
## Hazards
* Undesired behavior in waveform, though not logically incorrect
### Eliminating Hazards Method 1
* Redundant implicant to cover transition
* Output no longer depends on the c-transition
  * Systematic solution
* Adds logic gate (less efficient)
### Eliminating Hazards Method 2
* Make sure delay of paths match to remove glitch
  * cX timing is same as cN
## Recap of Course Material
* Intro to digital design
  * Digital representation of info
  * Boolean algebra
  * Logic design CAD tool
* Combinatorial logic design
  * Representations
    * English, trush table, minterm list, equation, cubes, k-map
  * K-map minimization: prime implicants, distinguished minterms, cover
  * Don't cares
  * Sum-of-products, product-of-sums
## One-Hot Representation
* N elements represented with N bits
* Exactly one bit is set
## Decoder
* Decoder converts symbols from one encoding to another
* Binary to one-hot decoder 
### Implementing Arbitrary Logic Functions with Decoders
* Example: primer number function
* Compute the output as the OR of the required minterms
* Useful to note: since the decoder is made with ANDs, we are building the sum-of-products
## Encoder: Inverse of a Decoder
* Logic module that convers one-hot input signal to a binary-encoded output signal
