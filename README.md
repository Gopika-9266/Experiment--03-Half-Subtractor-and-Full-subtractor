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

module halfsubtractor(a,b,difference,borrow);
inputs a,b;
outputs difference,borrow;
wire x;
xor(difference,a,b);
not(x,a);
and(borrow,x,b);
endmodule



module halfsubtractor(a,b,difference,borrow);
inputs a,b;
outputs difference,borrow;
wire x;
xor(difference,a,b);
not(x,a);
and(borrow,x,b);
endmodule



Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Gopika.R
RegisterNumber: 22009266 


## Output:


## Truthtable:


![images](https://user-images.githubusercontent.com/122762773/214631076-25d9d019-ff5b-4352-9cbe-e97af1f8ec76.png)


![full-subtractor2](https://user-images.githubusercontent.com/122762773/214631197-cc01b461-f312-46cd-96d0-62574f686d20.png)


##  RTL realization:


![Screenshot (85)](https://user-images.githubusercontent.com/122762773/214631417-1a39af73-66d2-4c95-bbe8-a57e94f9aff9.png)


![Screenshot (20)](https://user-images.githubusercontent.com/122762773/214631576-1e524675-fc68-4f96-b463-aede22f55296.png)


## Timing diagram:


![Screenshot (19)](https://user-images.githubusercontent.com/122762773/214631830-74cba64d-56ec-488d-be2b-bc9e9bff23ad.png)


![Screenshot (21)](https://user-images.githubusercontent.com/122762773/214632018-daaff4be-9837-4231-851e-aac112df5f45.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
