Developed by:V Sandhiya 
RegisterNumber:22007409  

AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.
Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors. 
Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
Diff = X'Y+XY' = X ⊕ Y
Borrow = X'Y
![sandy1](https://user-images.githubusercontent.com/121559414/211149770-4f5cde38-c0c4-4cc3-a1e8-3210d0a22b9c.png)



Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: 
minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure




Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule

LOGIC GATES:
![sandy3](https://user-images.githubusercontent.com/121559414/211149581-79ae2dac-a649-4ef2-bad3-96edc66854d7.png)


## Output:
## Truthtable:

HALF SUBTRACTOR

![sandy4](https://user-images.githubusercontent.com/121559414/211149232-4a197a42-3588-4b5d-9f8d-24c18c832f07.png)

FULL SUBTRACTOR

![sandy5](https://user-images.githubusercontent.com/121559414/211149249-6add0fa2-1526-4d1a-b2e0-7cde93d1451d.png)



##  RTL realization
HALF SUBTRACTOR

![sandy6](https://user-images.githubusercontent.com/121559414/211149284-ce8368c3-8bcf-407c-a796-63d9ca31c67c.png)

FULL SUBTRACTOR
![sandy7](https://user-images.githubusercontent.com/121559414/211149296-19f5ff7d-2490-4f02-8075-a0814d6c3d51.png)



## Timing diagram 
HALF SUBTRACTOR

![sandy8](https://user-images.githubusercontent.com/121559414/211149384-5389c34e-afdc-4ca0-ab5e-9beae6e8038c.png)
FULL SUBTRACTOR

![sandy9](https://user-images.githubusercontent.com/121559414/211149455-11c19b11-2517-4385-adb6-7242797671c3.png)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
