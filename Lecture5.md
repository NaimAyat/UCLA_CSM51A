# Lecture 5: April 16, 2018
## Logistics
* Quiz first 30 mins of class Monday, April 23
## Verilog
### Modules - Basic Building Block
* Two ways to instantiate
  * `BB8` - passes in overriding parameters (in order)
  * `BB10` - port ordering matters
### Representation of Signals, Numbers, and Variables
* Numbers represented as `<length>'<base><value>`
  * Examples: `8'b000100111`, `2'hFF`, `8'b001_0111` (underscore allowed to improve readability)
  * Undefined: `x` represents uncertainty, usually because two nodes are driving the same bit and conflicting
  * High impedance: not driven by an output `z`
