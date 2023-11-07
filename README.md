# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

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

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Anandhamoorthy.k
RegisterNumber:  212222100004
Half adder program:
module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum= A^B;
assign carry = A&B;
endmodule
Full adder program:
module FullAdder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
*/
```
### Output:
### RTL:
## HALF ADDER:
![Screenshot 2023-09-14 183826](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/672e2a28-1514-48ff-bf68-382f7afdbb61)

## FULL ADDER:
![Screenshot 2023-09-14 183819](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/57278865-3617-4715-ac95-e4b176b2d3da)
### TRUTH TABLE :
## HALF ADDER:
![Screenshot 2023-09-14 183751](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/b4194f8a-7da9-4c95-8350-1e38b5566c39)
## FULL ADDER:
![Screenshot 2023-09-14 183805](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/0554bf43-f193-4a9c-b7dc-fcd12ce5f717)
### WAVEFORM:
## HALF ADDER:
![Screenshot 2023-09-14 183738](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/7668b6d4-0731-4a7a-a10a-59366f0666c5)
## FULL ADDER:
![Screenshot 2023-09-14 183706](https://github.com/AnandhamoorthyKarthikeyan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475998/b6fee734-f798-46f3-8804-692cf3791ec7)
### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
