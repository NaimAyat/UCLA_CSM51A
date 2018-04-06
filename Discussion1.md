# Discussion 1: April 4, 2018
## Overview
* TA office: T 2-3pm Eng IV 67-12
* Intro
* Binary representation
* Noise margin
* Boolean algebra
## Representation
* Binary 
  * Multiple bits to represent multiple states
  * If we have n buts, we can represent 2<sup>n</sup> states
  * Right-most bit = most significant bit (MSB)
  * Left-most bit = least significant bit (LSB)
  * V<sub>IH</sub> minumum input voltage represented as a 1
  * V<sub>IL</sub> maximum input voltage represented as a 0
  * V<sub>OH</sub> minimum output voltage represented as a 1
  * V<sub>OL</sub> maximum output voltage represented as a 0
  * V<sub>IH</sub> < V<sub>OH</sub>
  * V<sub>IL</sub> > V<sub>OL</sub>
  * Difference V<sub>OH</sub> - V<sub>IH</sub> = noise margin high (V<sub>NH</sub>)
## Discrete vs. Analog Representation
* Tradeoff: noiseless vs. data density
## Types of Binary Representations
* 8 states
  * Plain: 000, 001, 010, 011, 100, 101, 110, 111
  * Thermometer: 0000000, 0000001, 0000011, 0000111, 0001111, 0011111, 0111111, 1111111
  * One-hot: 00000001, 00000010, 00000100, 00001000, 00010000, 00100000, 01000000, 10000000

## [Practice Problems](practiceProblems/week1.pdf)
* 1.11. (i) Need 6 bits (ii) Need 4 bits to represent cards ace through king, plus 2 bits to represent the four different suits
* 1.2. (a) 0.5V (b) 0.3V (c) 0.4V, since V<sub>OH</sub>-V<sub>IH</sub> = 0.4V (d) Assuming V<sub>DD</sub> = 2.5V, answer is 0.3V.
