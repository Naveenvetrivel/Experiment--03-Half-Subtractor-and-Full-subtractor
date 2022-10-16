# Experiment--03-Half-Subtractor-and-Full-subtractor
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



Write the detailed procedure here 


## Program:
~~~
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: NAVEENKUMAR V
RegisterNumber:  212221230068
### Half Subtractor:
module halfsub(A,B,diff,barrow);
input A,B;
output diff,barrow;
wire x;
xor(diff,A,B);
not(x,A);
and(barrow,x,B);
endmodule

### Full Subtractor:
module fullsub(A,B,C,diff,barrow);
input A,B,C;
output diff,barrow;
assign diff = A ^ B ^ C;
assign barrow = ~A & (B^C) | B & C;
endmodule
*/
~~~

## Output:

## Truthtable
## HALF SUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047003-d71c2789-675c-4a1a-acec-2afc931bb5ce.png)
## FULLSUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047015-e76ba302-f947-4361-aab0-33744b5cf517.png)

##  RTL realization
## HALF SUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047042-8125f809-9584-47d6-b7be-bc160985cbc9.png)
## FULL SUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047050-8f7bfeba-ca37-48e6-809c-0d2bac2f791c.png)


## Timing diagram 
## HALF SUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047068-acda591e-9ed7-4eb7-b1d3-edf107e8a80f.png)
## FULL SUBTRACTOR:
![image](https://user-images.githubusercontent.com/94165322/196047074-910c776f-380b-4ca7-9b50-6ed6a964da96.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
