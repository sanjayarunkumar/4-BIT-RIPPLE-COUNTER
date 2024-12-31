# 4-BIT-RIPPLE-COUNTER
**AIM:**

To implement  4 Bit Ripple Counter using Verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**
Quartus prime

**THEORY**
**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations generate the timing diagram.

**PROGRAM**
### Developed by: SANJAY A  Register Number:24010848
```
module ripple_counter(
     input wire clk,
	  input wire rst,
	  output reg[3:0] count
	  );
	  
always @(posedge clk or posedge rst)
begin
     if(rst)
	     count <= 4'b0000;
	  else 
	     count <= count + 1;
end 
endmodule
```
**RTL LOGIC FOR 4 Bit Ripple Counter**
![330457800-f894ec00-35ff-42aa-91d4-33a3c4f83828](https://github.com/user-attachments/assets/283952b0-0461-4172-aec5-873818e2f011)

**TIMING DIAGRAMS FOR 4 Bit Ripple Counter**
![330457234-bf1e161f-d49e-4f1c-91d4-bed3185e20cf](https://github.com/user-attachments/assets/705c62d8-4cf8-406b-a3d7-22ef1f66c077)

**RESULTS**
Thus implementing 4 Bit Ripple Counter using Verilog and validating their functionality using their functional tables is done successfully.
