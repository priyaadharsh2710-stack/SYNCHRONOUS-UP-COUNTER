### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
module ex7 (out,clk,rstn); 
input clk,rstn;
output reg [3:0] out;
always @ (posedge clk)
begin 
	if(!rstn) 
		out<=0; 
	else 
		out <= out+1; 
end 
endmodule
```
Developed by: Priyadharshini V

RegisterNumber: 25018161


**RTL LOGIC UP COUNTER**
<img width="1113" height="400" alt="329460348-3fc75b05-1906-4744-8b66-a1245f6ef8dd" src="https://github.com/user-attachments/assets/3d07ba2d-0ae4-46b6-93e0-8aca73b9e39a" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1910" height="456" alt="329460454-6958c1cc-55d0-45b0-ae98-f11cf7b425ad" src="https://github.com/user-attachments/assets/2fb45d69-6cce-42d7-a38d-2cff81e39098" />


**TRUTH TABLE**

<img width="488" height="464" alt="image" src="https://github.com/user-attachments/assets/f5f17a53-45ce-40ff-8661-70f30cba4b9a" />

**RESULTS**

The 4 bit synchronous up counter have been implemented and validated its functionality successfully.
