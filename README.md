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


![image](https://github.com/user-attachments/assets/285bc36b-ad23-4525-8583-2136301eff04)





![image](https://github.com/user-attachments/assets/d8603e02-2e3c-4e85-a3bf-e2ae7c14b400)



**Procedure**
```
 1)Open Quartus2

2)open new file

3)create veri log file and using tools view the logic diagram

4)Then click on netlist viewer and press RTL viewer to view the OUTPUT in graph format
```

**Program:**
```
i)FULL ADDER 
module fa(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
ii)FULL SUBTRACTOR 
module fs(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
end module

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: JASHWIN.S
RegisterNumber:212224040131
*/
```
**RTL Schematic**


![image](https://github.com/user-attachments/assets/80772b7b-0edb-4dc7-8b82-ca5e82a8fb0c)



![image](https://github.com/user-attachments/assets/9f8a01bd-29f4-4588-b646-921e7b6da2f6)


**Output Timing Waveform**


![image](https://github.com/user-attachments/assets/ae175824-a146-4bbf-89fb-5bcf570ba9c0)


![image](https://github.com/user-attachments/assets/9f531a91-7631-440c-a708-0eb007d60000)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



