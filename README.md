# HALF_ADDER_SUBTRACTOR



Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

![Screenshot 2024-12-08 201753](https://github.com/user-attachments/assets/c1cbc464-f350-489e-84f6-beb14c758799)
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![Screenshot 2024-12-08 201814](https://github.com/user-attachments/assets/8a96297b-7441-4f05-bf40-8e27ccd94f8e)


Figure -01 HALF ADDER

**Half Subtractor**

![Screenshot 2024-12-08 201838](https://github.com/user-attachments/assets/9f1cf4e1-298f-487c-8800-551f262c16ea)





The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

![Screenshot 2024-12-08 201900](https://github.com/user-attachments/assets/1914782b-29d8-4aa3-be55-fcff416eb2da)



Figure -02 HALF Subtractor

**Truthtable**

![Screenshot 2024-12-08 202511](https://github.com/user-attachments/assets/d9d8bc8f-1e27-409c-b1e1-1a34c26d3bc0)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
module exp3(a,b,cy, sm, df,bo);<br>
 input a,b;<br>
 output sm,cy, df, bo;<br>
 xor(sm,a,b);<br>
 and(cy,a,b);<br> 
 xor(df,a,b); <br>
 and (bo,~a,b);<br>
 endmodule<br>

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:Lokesh. M<br> RegisterNumber:24900227

**RTL Schematic**

![Screenshot 2024-12-08 202637](https://github.com/user-attachments/assets/9ecb488e-a797-4b7d-9470-fa21e3b65b6a)


**Output/TIMING Waveform**


![Screenshot 2024-12-08 202829](https://github.com/user-attachments/assets/b7f40098-a203-4000-8c2f-86383dd2ed0d)

**Result:**
 The truth table for half adder and half subtracter are verified successfully.
