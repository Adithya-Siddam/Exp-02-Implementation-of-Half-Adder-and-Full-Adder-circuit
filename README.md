# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -02 HALF ADDER:


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)


### Procedure:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: S Adithya Chowdary.

RegisterNumber: 212221230100.
### Half Adder:
~~~
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
~~~
### Full Adder:
~~~
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
~~~
### Output:
### Half Adder:
### RTL:
![image](https://user-images.githubusercontent.com/93427248/196044511-ebe5f280-1aa3-4972-b6b7-11f3bf5f58e7.png)

### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/93427248/196044521-8b3c7268-c2a6-4712-928f-ffdc7c226af1.png)

### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/93427248/196044550-00ade3ac-491e-4b6b-8192-3d4fdf1442cd.png)
### Full Adder:
### RTL:
![image](https://user-images.githubusercontent.com/93427248/196044608-6bbc11f3-f0ba-44a4-b616-cd0a0cd0e405.png)
### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/93427248/196044628-d8320b8a-3891-415c-aa54-7c2483ea1e4a.png)
### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/93427248/196044647-caa255f3-0d73-4f05-beb7-1589dd6d0dbc.png)
### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.


