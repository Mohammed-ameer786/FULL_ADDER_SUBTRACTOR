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


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
**FULL ADDER**
```
module full_adder (
   input  wire a, b, cin,   // Inputs
   output wire sum, carry   // Outputs
);

   // Logic equations
   assign sum   = a ^ b ^ cin;                  // XOR for sum
   assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
**FULL SUBTRACTOR**
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```
Developed by:F. MOHAMMED AMEER 
RegisterNumber:25015295


**RTL Schematic**
**FULL ADDER**

<img width="1562" height="848" alt="Screenshot 2025-11-22 112427" src="https://github.com/user-attachments/assets/bf1196a4-b5f3-4e09-9c2f-616f5a2dc89a" />


**FULL SUBTRACTOR**

<img width="1174" height="367" alt="Screenshot 2025-11-22 112529" src="https://github.com/user-attachments/assets/21b67a61-7c5e-4cad-a444-eef23264d351" />

**Output Timing Waveform**
**FULL ADDER**
<img width="1070" height="299" alt="Screenshot 2025-11-22 112636" src="https://github.com/user-attachments/assets/ff3e338a-c443-420c-890f-130372b10a24" />
**FULL SUBTRACTOR**
<img width="1067" height="314" alt="Screenshot 2025-11-22 112700" src="https://github.com/user-attachments/assets/aa85e3cf-653d-42ad-824b-17ff97e286b3" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



