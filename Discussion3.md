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
  wire y4 = y5;
  ```
* Conditional assignment
  ```
  /* If x1 = x2, then x3 is one */
  assign x3 = (x1==x2)?1'b1:1'b0;
  ```
* Bitwise vs. logical operators
  * Bitwise operators: `&`, `|`  
  * Logical operators: `&&`, `||`
  ```
  assign x1 = 4'b0110;
  assign x2 = 4'b1000;
  assign x3 = x1 | x2; //x3 = 4'b1111
  assign x3 = x1 || x2; //x3 = 1'b1
  ```
* Modules
  ```
  ModuleName m1 (.a1(a1_1), .a2(a2_1)));
  ModuleName m1 (a1_1, a2_1);
  ModuleName m2 (.a1(a1_2), .a2(a2_2)));
  ```
* `always` blocks
  * Combinational logic or sequential logic
    * Combinational:
      ```
      always @ (*)begin 
      
      end
      ```
    * Sequential:
      ```
      always @ (negedge rst or posedge clk)begin
      
      end
      ```
* Non-blocking assignment (best for sequential logic)
  ```
  x1 <= x2;
  ```
* Blocking assignment
  ```
  x1 = x2;
  ```
* If-else
  ```
  always (*) begin
  
  if (conditional) begin
  
  end
  
  else if (condition2) begin
  
  end
  
  else begin
  
  end
  
  end
  ```
* Case
  ```
  case (x1)
  4'0000: xxx: yyy=aaa; //x1 is 4 bits and equal to 0000
  4'0001: xxx: yyy=bbb; //x1 is 4 bits and equal to 0001
  
  default: yyy=qqq;
  endcase
  ```
