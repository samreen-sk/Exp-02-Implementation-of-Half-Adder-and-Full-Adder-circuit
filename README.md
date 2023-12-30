# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit
# NAME: Shaik Samreen
# REGISTER NUMBER: 23013412

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Procedure
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

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

### PROGRAM
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Shaik Samreen
RegisterNumber:  23013412
### half adder
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule
### full adder
module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
*/

### Output:
# logic symbol & truth table:
## half adder
![293334002-603405d1-6e6a-4e25-9d41-21ee7486e47c](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/c04aebdf-47e0-43ad-9a45-c16c5c308df4)
## full adder
![293334170-96ddd1a1-710e-44de-9d4f-0ec40ca49195](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/1569df39-e377-43e9-83ab-cfc72c6504c1)

### RTL realization
# half adder:

![293334393-eddf84e3-d5bc-4ef5-9a73-ed83e5759da1](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/4bcb0f46-a5a9-4d9e-b7ba-5c07ced29529)
# full adder:
![293334589-526b9bdd-2746-4236-aefb-2c7cbf2ff453](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/a61aaec3-e630-4701-8def-80bbb8f06dcf)

### TIMING DIAGRAM
## half adder:
![293334733-81757a56-2747-47c2-b7ac-4c1ac8bc3c4c](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/6fba4301-04e7-46f2-b9b7-d4a6992db95e)
## full adder:
![293334893-36a9174d-ef20-4010-a456-15194746754d](https://github.com/samreen-sk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347632/f731c8ff-045a-4397-ac61-95241345ab44)

### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
