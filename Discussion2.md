# Discussion 2: April 13, 2018
## Overview
* Rmap
* Decoder/Encoder
* Expression -> Truth Table
* Simplification -> schematic
## Definitions
* Implicant: product term, indicates output = 1
* Prime implicant: obtained by combining maximum possible numbers in adjacent squares
* Essential implicant: minterm that's only covered by one prime implicant
1. Find prime implicants
2. Identify essential implicants
3. Select essential implicants first, then use the least prime implicants to cover all the terms
* Express in POS
  1. Find SOP of logic 0
  2. Apply De Morgan's Law
## ![Problems](practiceProblems/week2.pdf)
### Ex. 3.23
* Simplify (~x ^ y ^ ~z) v (~x ^ ~y ^ ~z) v (x ^ ~y ^ ~z)
  * (~x ^ y ^ ~z) v (~x ^ ~y ^ ~z) v (~x ^ ~y ^ ~z) v (x ^ ~y ^ ~z)
  * Combine: (~x ^ ~z) v (~y ^ ~z)
  
