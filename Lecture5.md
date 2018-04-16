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
### Declarative Statements
* Provide logical relations between iputs and outputs
* Assign outputs to be some continuous function of the inputs
* Uses C-like syntax
* Outputs are wires, and can be single or multiple bits
#### Order of Execution
* Don't assume any particular order, as each statement occurs concurrently. For example:
  ```
  assign     x = aaa;
  assign     aaa = bbb;
  ```
### Procedural Statements
* Still needs flow contol statements (implies sequential ordering)
  * Denoted with keyword `always` or `initial` provides functionality of a program that executes sequentially
* `initial`
  * Purely behavioral for test bench
  * The sequence that is run only at the beginning of execution
* `always`
  * Can be synthesized: each block is run concurrently and executed when activated
  * LHS must be declared as registers, RHS can be registers or wires
* Inside an `initial` or `always` block, can use standard confrol flow statements
  ```
  if (<conditional>) then
    <statements>; //statements can be compounded by using begin <statements>; end
  else
    <statements>;
  case (<var>)
    <value>:<statements>
  ```
