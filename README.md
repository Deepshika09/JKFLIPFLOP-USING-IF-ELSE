
# JKFLIPFLOP-USING-IF-ELSE
### Deepshika hemanth kumar
### 212224220020
*AIM:* 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

*SOFTWARE REQUIRED:*

Quartus prime

*THEORY*

*JK Flip-Flop*

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

*Procedure*

1.Open Quartus Prime and create a new project.

2.Create a new Verilog HDL file and name it jk_flipflop.v.

3.Write the JK Flip-Flop code using if-else statements.

4.Save the file and add it to the project.

5.Compile the project to check for errors.

6.Open the Simulation Waveform Editor (or ModelSim) to simulate.

7.Apply various inputs (J, K, CLK, RST) and observe output Q.

8.Compare the outputs with the JK flip-flop truth table.

9.Save your design and submit results/report.

*PROGRAM*




module exp7(J,K,clk,q,qbar);
input J,K,clk;
output reg q;
output reg qbar;
initial q=0;
initial qbar=1;
always@(posedge clk)
begin
q=(J&(~q)|(~K)&q);
qbar=~q;
end
endmodule


*RTL LOGIC FOR FLIPFLOPS*

![Screenshot 2025-04-16 153511](https://github.com/user-attachments/assets/cd32a82e-b2b5-4a0c-a602-c044ade8eb6e)


*TIMING DIGRAMS FOR FLIP FLOPS*

![Screenshot 2025-04-16 154542](https://github.com/user-attachments/assets/2c24bffe-3cbb-4623-9111-0b0ac2798809)


*RESULTS*

Designed and verified the implimentation of JK flipflop circuit and truthtable in quartus ii using verilog programming successfully.
