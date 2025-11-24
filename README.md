# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
~~~
***Half-adder***
module expadd(a,b,sum,carry);

input a,b;

output sum, carry;

xor g1(sum, a,b);

assign carry =a&b;

endmodule

***Half-subtractor***
module exp3 (a,b, diff, borrow);

input a,b;

output diff, borrow;

xor g1(diff, a,b);

assign borrow =~a&b;

endmodule
~~~

Developed by:Muhammad Irfan M RegisterNumber:25014471

**RTL Schematic**
<img width="1772" height="942" alt="image" src="https://github.com/user-attachments/assets/6b2e0e7f-84ab-4ef6-80c5-ac2fc49d3f53" />
<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/7b7c607e-0cff-4611-9ddd-47ef17ad6999" />



**Output/TIMING Waveform**
<img width="1910" height="993" alt="image" src="https://github.com/user-attachments/assets/380bb434-6d13-4c72-a429-b7151be1d6fb" />
<img width="1912" height="1011" alt="image" src="https://github.com/user-attachments/assets/f62197bd-19a5-4842-ba66-3d614c64e2b3" />




**Result:**
Thus designed a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.
