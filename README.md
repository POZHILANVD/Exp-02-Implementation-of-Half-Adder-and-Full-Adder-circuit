# Name: POZHILAN V D
# Roll No: 23013442
# Experiment 03: Implementation of Half Adder and Full Adder circuit
# AIM
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.
# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime
# Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

# Procedure

Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.






# Program:
### Half adder
module HalfAdder(a,b,sum,carry);

input a,b;

output sum,carry;

assign sum=a^b;

assign carry=a&b;

endmodule

### Full adder
module Fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum=((a^b)^c);

assign carry=((a&b) | (b&c) | (c&a));

endmodule

# RTL realization
### Half adder
![HALF RTL](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/83aa836b-b21d-492e-b65c-1a4b7a4bdf0d)


### Full adder
![FULL RTL](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/cd664b57-1e54-4350-b17e-bffaf877742f)


# Truth Table
### Half adder
![HALF TRUTH](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/06320a79-13c2-45a4-b457-9fecc73611a2)

### Full adder
![FULL TRUTH](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/fdadfe63-e1e3-480a-bc50-5ee704ded449)


# Timing Diagram
### Half adder
![HALF TIME](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/2f250007-25f5-454c-aca5-2c5c4505a2ff)


### Full adder
![FULL TIME](https://github.com/POZHILANVD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870498/8c1f855d-562c-439d-b8c3-ae1d13721f4a)


# Result
Hence, the output is verified successfully.
