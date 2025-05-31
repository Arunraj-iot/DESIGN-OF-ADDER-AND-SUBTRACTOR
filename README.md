# FULL_ADDER_SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit

## Arunraj R
## Reg no: 212224110006

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

1.FULL ADDER:

![image](https://github.com/user-attachments/assets/d3a931e6-4a87-4338-8645-0a4142fb0432)


2.FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/c24e36af-189f-4ba9-b2fd-15f6801d26a0)

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

``` 
Developed by   : Anbuselvan S  
RegisterNumber : 212223240008
```

```verilog
//Full adder

module full_add(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b)|((a^b)&cin));
endmodule
```

```verilog
//Full subtractor

module full_sub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=((~a&b)|(~(a^b)&bin));
assign borr=((~a&b)|(b&bin)|(~a&bin));
endmodule
```

**RTL Schematic**

1. FULL ADDER

![image](https://github.com/user-attachments/assets/2457f745-8df4-45a9-9192-f455fe055c1b)


2. FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/fd079400-7437-423c-b24c-85117651a92f)


**Output Timing Waveform**

1. FULL ADDER

![image](https://github.com/user-attachments/assets/3c4cabe8-1b2f-4dde-baf3-46379770a3e6)


2. FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/39f67a82-2e6f-41cc-875c-abc294f85958)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
