# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: karthikeyan M 
RegisterNumber:212223040088
*/
```
module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```
**RTL realization**
![Screenshot 2024-03-23 231556](https://github.com/Aadithya2201/BOOLEAN_FUNCTION_MINIMIZATION/assets/145917810/2f2ee9a5-8145-4b7f-95ec-bb5b988f174f)

![Screenshot 2024-03-23 231605](https://github.com/Aadithya2201/BOOLEAN_FUNCTION_MINIMIZATION/assets/145917810/7b7487a8-722f-4c8a-9fa4-59f32b67a57a)

**Output:**

**Truth Table**
![Screenshot 2024-03-23 231625](https://github.com/Aadithya2201/BOOLEAN_FUNCTION_MINIMIZATION/assets/145917810/542b25de-f19b-417f-8d74-176a3cdce277)
![Screenshot 2024-03-23 231641](https://github.com/Aadithya2201/BOOLEAN_FUNCTION_MINIMIZATION/assets/145917810/5b739f91-f411-4c02-940a-954a85bf29b7)

**Timing Diagram**
![Screenshot 2024-03-23 231658](https://github.com/Aadithya2201/BOOLEAN_FUNCTION_MINIMIZATION/assets/145917810/a2ed349d-ac3c-44b5-a177-4756107a165a)

**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

