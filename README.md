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

**Full Adder**

![WhatsApp Image 2024-12-21 at 09 58 42_90a8f72b](https://github.com/user-attachments/assets/ee5a9898-0bf0-446f-b94c-80854af6656d)


**Full Subtractor**

![WhatsApp Image 2024-12-21 at 09 59 01_1159e08f](https://github.com/user-attachments/assets/5b1297be-8ec4-4987-9df7-d9318f5617f7)


**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.
   
**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Full adder

//full adder
module full_add(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire s1,c1,c2;


//instantiate logic gate primitives
xor (s1,a,b);
and (c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);


endmodule

Full subtractor

module full_sub (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=^bin;
assign bo=w2|w3;
endmodule
```

Developed by:Thilak raaj .P 

RegisterNumber:24900585


**RTL**
![Screenshot 2024-11-05 142611](https://github.com/user-attachments/assets/3107b83c-8de1-42e9-b5fc-33e0d4a8581f)
![Screenshot 2024-11-05 144004](https://github.com/user-attachments/assets/6caef989-4996-40c4-b9de-373a4cd71669)

**Output Timing Waveform**
![Screenshot 2024-11-05 143802](https://github.com/user-attachments/assets/fb40bf17-f250-40bf-bcea-d0916fe34351)
![image](https://github.com/user-attachments/assets/2353d5e3-0e19-4571-9923-6239281345ec)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



