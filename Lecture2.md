# Lecture 2: April 4, 2018
## Binary Representations of Discrete Information
* How would you select a representation?
  * Choose based on implementation
  * How many bits are needed to represent days of the year?
    * 9 bits, there are 365 days in year and 2<sup>9</sup> = 512
* Binary is essentially saying a certain range in voltage represents a 0 and a certain range represents a 1
### Noise in Analogy and Digital Signals
* Analog: noise added to input, input faithfully reproduced (noise in output)
* Digital: noise added to input, no noise in output
  * Output constrained in a smaller range than the input range
### TTL Logic (Transistor-Transistor Logic)
* Noise that can be handled in low threshold (0) = input low - output low = V<sub>IL</sub> - V<sub>OL</sub>
* Noise that can be handled in high threshold (1) = input high - output high = V<sub>IH</sub> - V<sub>OH</sub>
* Noise margins not necessarily symmetric
* V<sub>DD</sub>: supply voltage, theoretically battery voltage; in practice slightly lower
### CMOS (Complementary Metal–Oxide–Semiconductor) Logic
* Modern standard
* Noise margins symmetric
### Combinational Logic
* Output is a function of current input
* Memoryless
#### Closure Property
* Combinational logic circuits are closed under acyclic composition
  * Writing combinational circuits without creating loops in the circuit yields another type of combinational circuit
