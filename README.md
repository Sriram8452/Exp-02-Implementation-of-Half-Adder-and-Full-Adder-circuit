# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware - PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
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

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
Developed by: Sriram G
RegisterNumber:212222230149
### Half Adder
```
module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum= A^B;
assign carry = A&B;
endmodule
```
### Full Adder
```
module FullAdder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
```
### Output:
### RTL
![1](https://github.com/Sriram8452/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118708032/b12116c3-933d-4d26-8b92-8b1fc3450267)
![2](https://github.com/Sriram8452/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118708032/94b43708-123d-469b-8f40-53c127139895)
### TIMING DIAGRAM
![3](https://github.com/Sriram8452/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118708032/362a944d-6a41-435e-a8c3-35f3cb20dceb)
![4](https://github.com/Sriram8452/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118708032/50c68926-cd77-43d2-a4dc-212b19daab16)
### TRUTH TABLE 
![5](https://github.com/Sriram8452/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118708032/b4a0f992-3fb2-4de2-9672-d7ca28aff4d5)

### Result:
Thus a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog
programming

