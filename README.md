# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

Full_adder

![315924513-081ddba5-c4a4-4e59-b7ec-f0bca74e533a](https://github.com/Md-Afshan/FULL_ADDER_SUBTRACTOR/assets/147140059/ab4b8166-b57f-4630-a1f4-779e99e6e694)

Full_subtractor

![315924444-07276c8a-6060-4194-8294-a822c948800a](https://github.com/Md-Afshan/FULL_ADDER_SUBTRACTOR/assets/147140059/8a89c6f8-4e18-475f-a74b-3bcb3d9ad12a)

**Procedure**

## Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

## Full Subtractor: 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
## Full_adder
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```

## Full_subtractor
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
Developed by: Muhammad Afshan .A

RegisterNumber: 212223100035
*/

**RTL Schematic**

![315924267-bb5d6aba-b187-46b7-857d-617ac2d3ea89](https://github.com/Md-Afshan/FULL_ADDER_SUBTRACTOR/assets/147140059/f7092ea1-3fbb-437b-bab8-cf9a041c2e39)

**Output Timing Waveform**
Full_adder
![315924188-7ac86948-5e35-41f6-ab82-89d86938f436](https://github.com/Md-Afshan/FULL_ADDER_SUBTRACTOR/assets/147140059/d1fc14a0-98fe-4e27-83ca-3eceecd6cb68)


Full_subtractor
![315924042-47370fa6-6ee8-4273-bd2b-8e3f5eeb6c3b](https://github.com/Md-Afshan/FULL_ADDER_SUBTRACTOR/assets/147140059/84939484-4a83-4f7d-ab6b-1f7815d32887)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



