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

**Procedure**

Write the detailed procedure here

**Program:**
```
module exp4(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum =(a^b^c);

assign carry =(a&b)|(b&c)|(c&a);

endmodule
```
```
module exp4(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```
**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot 2025-11-19 112457" src="https://github.com/user-attachments/assets/338cc8cd-8519-4747-af01-5669b2033c57" />
<img width="1036" height="552" alt="Screenshot 2026-01-01 222849" src="https://github.com/user-attachments/assets/90c5c462-338f-4113-920d-37e1294778e2" />



**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot 2025-11-19 112651" src="https://github.com/user-attachments/assets/2554d642-e84a-4f36-a230-7b3f858249bd" />
<img width="1037" height="583" alt="Screenshot 2026-01-01 223107" src="https://github.com/user-attachments/assets/80c3d3aa-24cf-403b-8399-e39630a0220b" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



