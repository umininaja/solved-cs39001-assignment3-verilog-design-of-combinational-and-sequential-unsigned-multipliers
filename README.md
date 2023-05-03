Download Link: https://assignmentchef.com/product/solved-cs39001-assignment3-verilog-design-of-combinational-and-sequential-unsigned-multipliers
<br>



<ol>

 <li><strong>[Combinational Unsigned Binary Multiplier (</strong><em>Array Multiplier</em><strong>)] </strong>Design (using Verilog), simulate (using a proper Verilog testbench) and synthesize for any target FPGA platform supported by your version of <em>Vivado</em>,a combinational circuit (“Array Multiplier”) to multiply two 6-bit unsigned integers. For the general architecture of an array multiplier, please refer to the diagram uploaded on <em>Moodle</em>. Note down the hardware footprint and critical path delay of your synthesized design. The interface of your design should be:</li>

</ol>

module unsigned array mult (input [5:0] a, input [5:0] b, output reg [11:0]

product);.

<ol start="2">

 <li><strong>[Sequential Unsigned Binary Multiplier (left-shift version)] </strong>Consider the iterative multiplication</li>

</ol>

<em>n</em>−1                                                <em>n</em>−1

of two <em>n</em>-bit unsigned integers, <em>X </em>= <sup>X</sup><em>x<sub>j</sub></em>2<em><sup>j </sup></em>and <em>Y </em>= <sup>X</sup><em>y<sub>j</sub></em>2<em><sup>j</sup></em>, to form the 2<em>n</em>-bit product <em>P </em>= <em>X </em>· <em>Y </em>.

<em>j</em>=0                                                 <em>j</em>=0

Multiplication proceeds by calculating the partial products (associated with corresponding left-shifts) as: <em>P<sub>i</sub></em><sub>+1 </sub>= <em>P<sub>i</sub></em>+<em>x<sub>i</sub></em>2<em><sup>i</sup>Y </em>for each bit <em>x<sub>i </sub></em>of the multiplier, with <em>P</em><sub>0 </sub>= 0 and <em>P<sub>n </sub></em>= <em>P</em>. Design (using Verilog), simulate (using a proper Verilog testbench), and synthesize for any target FPGA platform supported by your version of <em>Vivado</em>, an <strong>6-bit sequential unsigned binary multiplier </strong>following the above scheme. The input-side operand registers used in the datpath of your multiplier should have “parallel load” capabilities such that the 6-bit operands can be loaded in each of them instantaneously. Note down the hardware footprint and critical path delay of your synthesized design. The interface of your design should be:

module unsigned seq mult LS (input clk, input rst, input load, input [5:0] a, input [5:0] b, output reg [11:0] product);, where the signal names suggest their functionality. (7 marks)

<ol start="3">

 <li><strong>[Sequential Unsigned Binary Multiplier (right-shift version)] </strong>Now, design, simulate, and synthesize for any target FPGA platform supported by your version of <em>Vivado</em>, the above multiplier using an alternative scheme that considers right-shifting of the partial products:</li>

</ol>

<em>P</em><em>i </em>= <em>P</em><em>i </em>+ <em>x</em><em>jY </em>and <em>P</em><em>i</em>+1 = 2−1<em>P</em><em>i</em>

The interface should be module unsigned seq mult RS (input clk, input rst, input load, input

[5:0] a, input [5:0] b, output reg [11:0] product);.

Other details remain the same.

– 2 –

<ol start="4">

 <li>Finally, submit a small 1-page report (in .pdf format) comparing the maximum speed of operation and hardware footprint of the above three designs. This report should be inside the zipped folder you submit.</li>

</ol>