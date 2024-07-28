This repository contains the Verilog code for a simple 16x8 RAM module. This RAM module can store 16 8-bit words and supports synchronous read and write operations.

📁 File Overview
ram.v: The Verilog module implementing the RAM.
🔍 Module Description
The ram module is designed to store and retrieve 8-bit data values at specific addresses. It has the following ports:

1. clk (input): Clock signal to synchronize the read and write operations.
2. rst (input): Active-high reset signal to initialize the memory contents and the output data.
3. we (input): Write enable signal that, when high, allows data to be written to the specified address.
4. addr (input): 4-bit address input to specify the memory location for read/write operations.
5. datain (input): 8-bit data input used during write operations.
6. dataout (output reg): 8-bit data output used during read operations.
   
Module Functionality

1. Resetting: When the reset (rst) signal is high, the output data (dataout) is set to zero (8'h00), and all memory locations are cleared.
2. Writing: If the write enable (we) signal is high, the data input (datain) is written to the memory location specified by the address input (addr).
3. Reading: If the write enable signal is low, the data at the memory location specified by the address input is read and assigned to the output (dataout).
