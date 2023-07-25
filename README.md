NAME : HARITHA RAMESH
REGISTER NO : 23003324
# Exp 02 Implementation of Half Adder and Full Adder circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program
### Half Adder
module halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor (sum,a,b);

and (carry ,a,b);

endmodule 

### RTL realization
![ha rtl](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/275a06c8-da3a-4c0e-b10b-be23185224b1)

### Truth Table 
![ha tt](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/a05c2af0-67d3-45d2-9dc0-915cc20bc671)
### WAVEFORM
![wf ha](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/865466ad-ff1b-4b89-929a-b4427ee7dab0)
### Program
### Full Adder
module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum, carry;

xor(sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule 
### RTL
![fa rtl](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/b4af36d6-a22d-4830-a335-72d0a5319a0a)
### Truth Table
![fa tt](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/ceb166ed-fb8b-4b82-969f-14cb3c3883dc)
### WAVEFORM
![wf fa](https://github.com/23003324/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035234/9502f44e-7749-430f-ae78-f8748d7885ba)
### Result:
Thus the given full adder and half adder are verified using verilog programming.
