Skip to content
nikkil-18
4-BIT-RIPPLE-COUNTER
Repository navigation
Code
Pull requests
Agents
Actions
Projects
Security and quality
Insights
You’re making changes in a project you don’t have write access to. Submitting a change will write it to a new branch in your fork kishoresundar20072007-max/4-BIT-RIPPLE-COUNTER, so you can send a pull request.
4-BIT-RIPPLE-COUNTER
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

4
Line wrap mode

Soft wrap
Editing README.md file contents
  9
 10
 11
 12
 13
 14
 15
 16
 17
 18
 19
 20
 21
 22
 23
 24
 25
 26
 27
 28
 29
 30
 31
 32
 33
 34
 35
 36
 37
 38
 39
 40
 41
 42
 43
 44
 45
 46
 47
 48
 49
 50
 51
 52
 53
 54
 55
 56
 57
 58
 59
 60
 61
 62
 63
 64
 65
 66
 67
 68
 69
 70
 71
 72
 73
 74
 75
 76

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

**PROGRAM**
```
module ripple_counter_4bit (
    input  wire clk,
    input  wire reset,
    output reg [3:0] q
);

    always @(posedge clk or posedge reset) begin
        if (reset)
            q <= 4'b0000;
        else
            q <= q + 1'b1;   // increments like a ripple counter
    end

endmodule
```


/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by
 RegisterNumber:
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**

<img width="655" height="215" alt="Screenshot 2025-12-15 182741" src="https://github.com/user-attachments/assets/89df138b-1ac9-4ebb-8a01-56e74612268a" />



**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

<img width="564" height="125" alt="Screenshot 2025-12-15 182844" src="https://github.com/user-attachments/assets/b11c2974-4392-4389-a7cf-c80e9ba9c9c3" />


**RESULTS**

    Thus To implement 4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is verified

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
