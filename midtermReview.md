# Midterm Review
## Binary Numbers
* In a base-two number system, the right-most bit represents ones, the second right-most bit represents twos, the third right-most bit represents fours, the fourth right-most bit represents eights, etc.
* For example, 64 is 1000000
### Two's Compliment
* Starting from the right, keep everything up to the LSB (the right-most 1). Flip the rest.
## Hexadecimal
* To convert binary to hex: split binary into groups of 4 bits, each group of 4 bits representing a number up to 16. Convert that number into a single character (0-9 A-G). Concatenate.
## Fixed Point
* After decimal, left-most bit is a half, second left-most is a quarter, third left-most is an eighth, etc.
## IEEE 32-Bit Floating Point Format
* Left-most bit is sign (1=neg), next eight are exponent, last 23 are mantissa
1. Represent left side of decimal in binary form
2. Represent right side of decimal in binary form
   * Multiply decimal part of original number by 2. Left side of result is bit. Right side gets multiplied by 2. Repeat until pattern found.
3. Concatenate steps 1 and 2. Shift decimal to the left to get into scientific notation. For each shift, multiply by two. For example, eight shifts requires the number to be multiplied by 2<sup>8</sup>
4. Convert to IEEE format.
   1. Sign bit: set as necessary
   2. Exponent: add scientific notation exponent to 127 (bias). Convert result to 8-bit binary
   3. Mantissa: take RHS of scientific notation. Stop mantissa at 23 bits to get 32 total bits.
### Misc
* Most positive number achievable in 2's compliment: 2<sup>bits-1</sup>-1. Most negative: -2<sup>bits-1</sup>
* Largest unsigned number achievable: 2<sup>bits</sup>-1
## Multiplexers
* Simply selects one of the inputs
  * Using selector variables
## Gray Code
* Convert binary to gray:
  1. Take down left-most bit
  2. XOR left-most bit with second left-most bit, write result. XOR second left-most bit with third left-most bit, write result...
## Boolean Algebra
* ![Logic simplification](https://qph.fs.quoracdn.net/main-qimg-729a869e39bf393f97e4c37d89594e8)
