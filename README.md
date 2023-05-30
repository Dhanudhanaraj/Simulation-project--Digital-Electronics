# DESIGN AND SIMULATE 8:1 MULTIPLEXER USING VERILOG

## AIM:

To design a 8:1 multiplexer and verify its truth table in Quartus using Verilog programming,validate its outputs.

## HARDWARE REQUIRED:

Hardware – PCs, Cyclone II , USB flasher.

Software – Quartus prime.

## Procedure

Step 1: Open Quartus Prime and select new project . Open new file at the verilog.

Step 2: Module Declaration. Module should have the file name.

Step 3: Input-Output Delecaration.

Step 4: Within the module, create a combinational logic block using a case statement to select the appropriate input based on the select inputs.

Step 5: End the module.

Step 6: Run the program and choose RTL viewer to get RTL realization.

Step 7: verifying the output by truthtable.

## THEORY:

### What is a Multiplexer

The multiplexer is a device that has multiple inputs and single line output. The select lines determine which input is connected to the output, and also increase the amount of data that can be sent over a network within a certain time. It is also called a data selector.

Multiplexers are capable of handling both analog and digital applications. In analog applications, multiplexers are made up of relays and transistor switches, whereas in digital applications, the multiplexers are built from standard logic gates. When the multiplexer is used for digital applications, it is called a digital multiplexer.

![asin](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/0d9bc980-f33b-4d49-a541-67c1eeece039)

The single-pole multi-position switch is a simple example of a non-electronic circuit of the multiplexer, and it is widely used in many electronic circuits. The multiplexer is used to perform high-speed switching and is constructed by electronic components.

### What is 8:1 Multiplexer

In the 8:1 multiplexer, there are total eight inputs, i.e., A0, A1, A2, A3, A4, A5, A6, and A7, 3 selection lines, i.e., S0, S1and S2 and single output, i.e., Y. On the basis of the combination of inputs that are present at the selection lines S0, S1, and S2, one of these 8 inputs are connected to the output. The block diagram and the truth table of the 8×1 multiplexer are given below.

![WhatsApp Image 2023-05-30 at 2 38 51 PM](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/64a99148-fe92-4569-a456-9c540d283470)

A multiplexer is a digital circuit that selects one input from multiple inputs based on the select inputs. The 8:1 MUX has 8 data inputs, 3 select inputs, and 1 output. The select inputs determine which data input is routed to the output. 

## TRUTH TABLE:

![WhatsApp Image 2023-05-30 at 2 38 51 PM (1)](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/1e1dfc6d-e377-4130-9950-127b0aeed3e6)

The logical expression of the term Y is as follows:

Y=S0'.S1'.S2'.A0+S0.S1'.S2'.A1+S0'.S1.S2'.A2+S0.S1.S2'.A3+S0'.S1'.S2 A4+S0.S1'.S2 A5+S0'.S1.S2 .A6+S0.S1.S3.A7

## LOGIC DIAGRAM:

Logical circuit of the above expression is given below:

![WhatsApp Image 2023-05-30 at 2 38 51 PM (2)](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/c976e4aa-822a-4f18-a228-43c6e2fb841d)

## PROGRAM:

```
NAME:DHANUMALYA D
REGISTER NUMBER:212222230030

module muxx(a,s,y);
input[7:0]a;
input[2:0]s;
output reg y;
always @ (a,s)
begin
   case(s)
   3'b000:y=a[0];
	3'b001:y=a[1];
	3'b010:y=a[2];
	3'b011:y=a[3];
	3'b100:y=a[4];
	3'b101:y=a[5];
	3'b110:y=a[6];
	3'b111:y=a[7];
   endcase
end
endmodule

```
## NETLIST DIAGRAM:

![DE SA21](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/5295fd6a-587a-494c-bc77-194905bb629d)

## TIMING DIAGRAM:

![DE SA-22](https://github.com/Dhanudhanaraj/Simulation-project--Digital-Electronics/assets/119218812/ad1554d3-cec3-4b65-a39e-74d25ec2289e)

## RESULT:

8:1 multiplexer has been implemented and its truth table in Quartus is verified by using Verilog programming,outputs are validated.
