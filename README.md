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

<img width="1536" height="1024" alt="ChatGPT Image Nov 22, 2026, 04_07_24 PM" src="https://github.com/user-attachments/assets/1799a240-3cb9-4763-ada8-e0cfc34b7801" />


**Program:**

~~~
module FullAddSub (
    input  a, b, cin,
    output sum, carry_out,
    output difference, borrow_out
);

assign sum        = a ^ b ^ cin;
assign carry_out  = (a & b) | (a & cin) | (b & cin);

assign difference = a ^ b ^ cin;
assign borrow_out = (~a & b) | (~(a ^ b) & cin);

endmodule
~~~

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: N.Surya

Register Number: 212225040442


**RTL Schematic**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a3033150-1609-461d-96bf-2336dd798c2a" />


**Output Timing Waveform**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f24aa996-8187-450e-abf9-c1d0fe5f1de2" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



