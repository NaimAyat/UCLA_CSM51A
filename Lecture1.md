# Lecture 1: April 2, 2018
## Logistics
* Office: MW 12-1PM at 56-147A in Engr IV
* Two in-class, closed-notes quizzes.
* Midterm: May 7, in-class. One 2-sided cheat sheet allowed.
* Final: June 14, two 2-sided cheat sheets allowed.
## Verilog
* https://www.edaplayground.com/
* (Optional) Dowload v0.9.7 from http://iverilog.icarus.com/
## Logisim
* Optional download, graphical tool for designing and simulating (v2.7.1)
* http://sourceforge.net/projects/circuit
## Module 2: The Digital Abstraction Representing Data Digitally
* Digital system: discrete-valued input signals enter digital system, which produces discrete-valued output signals
* Binary is a special case of discrete
* Question: what is a physical quantity is continuous?
  * Map it into a discrete form
  * Ex: sound waves are discrete but may look continous due to fine granularity (16-bit allows for 64000 levels)
* Question: what if information is complex?
  * Represent discrete information with binary signals; assign some sequence of 1s and 0s to represent more abstract concepts, like colors or characters
  * How many distinct elements can be represented in n bits? 2<sup>n</sup>
* A thermostat gets temperature readings from a sensor in the range of 68 to 82 degrees, and needs to know it to an accuracy (resolution) of 2 degrees. How would you represent it?
  1. Quantize the finite set
  2. Encode; 68 is 000, 70 is 001, and so on.
