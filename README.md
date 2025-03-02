# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: R.Vidhyadharan

RegisterNumber: 22008663
~~~py
module half_adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
~~~
~~~py
module full_adder(x,y,z,s,c);
input x,y,z;
output s,c;
wire x1,x3,x4;
xor(x1,x,y);
xor(s,x1,z);
and(x3,x,y);
and(x4,x,y);
or(c,x3,x4);
endmodule
~~~
### Output:
### RTL :
![half_adder_RTL_diagram](/half_adder.png)
![Full_adder_RTL_Diagram](/full%20add.png)
### TIMING DIAGRAM :
![half_adder_timing_diagram](/half_adder%20waveform.png)
![Full_adder_timing_diagram](/full_adder%20wave.png)
### TRUTH TABLE 
![half_adder_truthtable](https://user-images.githubusercontent.com/114286357/214351684-f220b25f-84fc-4646-bb47-8312a14f6248.png)

# Full ADDER
![full_adder_truthtable](https://user-images.githubusercontent.com/114286357/214351422-173d7ba9-9200-4553-8d83-434b5915ad4d.png)

### Result:
Thus the output of half_adder and full_adder experiment 
successfully achieved.
