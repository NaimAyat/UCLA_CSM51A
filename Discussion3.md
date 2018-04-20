# Discussion 3: April 20, 2018
## Verilog
* EDA Playground
* Define module and port name: 
  ```
  module aaa()

  endmodule
  ```
* Define input, output, and register
  ```
  input xxx;
  output yyy; //1-bit output
  output [4-1:0] yyy; //4-bit bus
  input a1, a2, a3;
  reg r1; //register
  reg [4-1:0] a2 [4-1:0];
  
  wire [8-1:0] y3;
  
  y3[3:0]
  ```
* Wire assignment
  ```
  wire [4-1:0]y4 = 4'b1110; //b means binary representation
  wire [4-1:0]y5 = 4'd12 //d means decimal (we need 4 bits to represent 12)
  ```
  
