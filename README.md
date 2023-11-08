# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Janani R
RegisterNumber:  2122212300399
*/
## HALF SUBTRACTOR:
```
module exp04(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor(difference,a,b);
not(x,a);
and(borrow,x,b);
endmodule
```
## FULL SUBTRACTOR:

```
module FullSub04(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
wire p;
assign difference=((a^b)^bin);
not (p,a);
assign borrow=((p&b)|(p&bin)|(b&bin));
endmodule
```

## Output:

Half Subtractor:

![image](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/48c2cef2-e711-49bd-aa3b-1438aea930ad)

Full Subtractor:

![image](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/41640ea2-b4c7-4373-b004-1bc1f158ebe6)

## Truthtable

Half subtractor:

![270082671-2d89af83-d022-415c-90e9-583daf67bae7](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/1e2db12c-5864-4cc5-9071-ce0983cbf722)

Full subtractor:

![270082689-f5e4b26b-f638-41b1-b22e-983f454d4bba](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/32b0915e-a3bf-4af1-bd6c-0a954b754dd1)

## output waveform

Half subtractor:

![270082712-7bea6682-50df-42d8-81c5-9018b01d2398](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/a4052fca-6b36-456d-8c74-96df5549710b)

Full subtractor:

![270082721-f6ce84c1-cb34-412b-a60c-f61f1792db28](https://github.com/Janani-2003/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/94288340/f5097db4-fe77-4f44-a35f-335d6eb9bdcb)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
