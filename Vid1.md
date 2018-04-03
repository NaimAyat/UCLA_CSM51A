# Video 1 & 2 Notes
* [Video 1](https://www.youtube.com/watch?v=pl25bK_PiGo)
* [Video 2](https://www.youtube.com/watch?v=B04fpj1xN5s)
## Video 1
* System: processes, stores, communicates signals
* Digital system: takes discrete input signals and outputs discrete output signals
  * Special digital systems: binary systems
* Binary samples are timed with a clock
  * Determines the rate at which information is being passed and processed
* Effect of noise on analog and digital signals
  * Analog signals may have error at output due to noise
  * Digital signals eliminate noise
## Video 2
### Ways to Represent Logic
* Propositional equations
* Truth table
* Logic gates
### Logic
* Any number of inputs and outputs
* Two types: combinatorial and sequential
### Combinational Logic (CL)
* Combinational when outputs are a direct functional mapping of inputs with no dependence on previous inputs of previous samples (no data storage)
### Sequential Logic
* Sequential when output (o[k:0]) values depend on both inputs (i[n:0]) and state (s[m:0]) of the logic based on previous inputs
### Combinational Truth Table
* n inputs = 2<sup>n</sup> entries
* "d" in a truth table represents "don't care"
### Closure Property - Hierarchically Composable
* Combinational logic circuits are closed under acyclic composition
  * Wiring combinational circuits without creating loops yields another combinatorial circuit
* Build up more complex combinational logic using building blocks
  * Break up complex logic into heirarchy of modules
### Common Types of Logic Gates
* [Logic gates](https://cdn-images-1.medium.com/max/1200/1*zq3cbyx-xd_SRq8EwzER0w.jpeg)
