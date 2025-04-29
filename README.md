# EXP-08 D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Draw the logic circuit diagram of a negative-edge triggered D Flip-Flop.

2.Connect the circuit using logic gates or IC on a breadboard/simulator.

3.Apply clock pulses and set the D input using switches or logic sources.

4.Observe the Q and Q̅ outputs on a logic analyzer or oscilloscope.

5.Verify output changes only at the falling edge of the clock.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: MITHUN S

RegisterNumber: 212224240088
*/
```
module exp8(D,clk,Q,Qbar);
input D,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=D;
Qbar=~D;
end
endmodule
```
**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/b2e57edd-d9c0-4538-8bc0-c85093ef10a9)


**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/23c6f21e-f2b0-40b9-a781-2b7b1cd32c06)



**RESULTS**

To implement D flipflop using verilog and validating their functionality using their functional tables is verified.
