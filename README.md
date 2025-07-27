# ARITHMETIC-LOGICUNIT-ALU-
COMPANY :CODTECH IT SOLUTIONS

NAME :KEERTHIS VIVIN

INTERN ID :CT04DH977

DOMAIN: VLSI

DURATION: 4 WEEKS

MENTOR : NEELA SANTOSH


DESCRIPTION:
im dividing this task one into two part one is verilog another is testbench by using MATLAB simulation tool

code 1:
This Verilog module, simple_alu, implements a tiny 4‑bit Arithmetic Logic Unit that operates purely combinationally. It accepts two 4‑bit unsigned inputs (A and B) and a 3‑bit opcode that selects the operation. The result is a 4‑bit reg, assigned inside an always @(*) block, which tells the synthesizer/simulator that the logic is combinational (i.e., it should re‑evaluate whenever any input changes). The ALU supports five operations: addition (opcode = 3'b000), subtraction (001), bitwise AND (010), bitwise OR (011), and bitwise NOT of A only (100). Any other opcode defaults the output to zero. Because all datapaths are only 4 bits wide, arithmetic naturally wraps around modulo 16; overflow/underflow flags are not produced, and high-order carries are silently discarded. Subtraction is two’s‑complement by construction (as in standard Verilog arithmetic), so A - B will also wrap modulo 16. The use of reg for result is just a Verilog storage type requirement for signals assigned in procedural blocks; it does not imply sequential logic, since there is no clock and no non‑blocking (<=) edge‑triggered assignment. The priority chain is written as an if/else if ladder; functionally this is equivalent to a case statement for mutually exclusive opcodes, but the given form is perfectly synthesizable. The NOT operation ignores B, which is typical for unary operations. 

code2:
TESTBENCH
The given Verilog module simple_alu_tb is a testbench written to verify the functionality of the simple_alu module. In digital design, a testbench acts as a virtual environment that applies different sets of inputs to the design under test (DUT) and observes the outputs to ensure that the module works correctly for all expected scenarios. Here, simple_alu_tb is designed to test all the five primary operations supported by the simple_alu module: addition, subtraction, bitwise AND, bitwise OR, and bitwise NOT.
Testbench Components

The testbench starts by declaring reg types for A, B, and opcode. These are the inputs to the ALU. The result is declared as a wire since it is an output that will be driven by the instantiated ALU. The naming convention and bit-widths match the design under test (A and B are 4-bit registers, opcode is 3-bit, and result is a 4-bit output).

The Unit Under Test (UUT), simple_alu, is instantiated using the module name and the uut label. The connections between the testbench and the ALU module are established using named port mapping (.A(A), .B(B), .opcode(opcode), .result(result)). This ensures that changes in A, B, or opcode from the testbench are immediately reflected in the ALU.



