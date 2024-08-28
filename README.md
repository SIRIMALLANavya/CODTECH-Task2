**Name:** Sirimalla Navya

**Company**: CODTECH IT SOLUTIONS

**ID:** CT08DS6727

**Domain:** VLSI

**Duration**: AUGUST to SEPTEMBER 2024

**Mentor**: NEELA SANTHOSH KUMAR

**OVERVIEW OF THE PROJECT**

**Project**: UART (UNIVERSAL ASYNCHRONOUS RECEIVER- TRANSMITTER) DESIGN

**Objective:**

Design a UART (Universal Asynchronous Receiver-Transmitter) receiver using VHDL, which can detect the start bit, receive data bits, and check the stop bit to ensure valid data reception.

**Key Points:**

1.Entity Declaration: Define the UART receiver entity with input clock, input serial data, output data valid, and output received byte signals.

2.State Machine: Implement a finite state machine (FSM) with five states: idle, start bit detection, data bits reception, stop bit detection, and cleanup.

3.Signal Declarations: Declare signals for the current state, clock counter, bit index, received byte, and data valid.

4.Process: Describe the behavior of the FSM using a VHDL process, which includes:

5.Start bit detection and timing

6.Data bits reception and storage

7.Stop bit detection and validation

8.Cleanup and preparation for next reception

**Output Assignments**: 

1.Assign the output signals data valid and received byte the values of the corresponding internal signals.

2.Clock Synchronization: Use the input clock signal to synchronize the FSM and ensure proper timing.

3.Bit Indexing: Use the bit index signal to keep track of the current bit position during data reception.

4.Data Validation: Use the stop bit detection and validation to ensure the received data is valid.

5.This is a VHDL implementation of a UART (Universal Asynchronous Receiver-Transmitter) receiver. Here's a breakdown of the code:

6.Entity Declaration

**The entity UART_RX has four ports:**

i_Clk: Input clock signal

i_RX_Serial: Input serial data signal

o_RX_DV: Output data valid signal

o_RX_Byte: Output received byte signal (8 bits)

Architecture

The architecture RTL (Register-Transfer Level) describes the behavior of the UART receiver.

State Machine

**The receiver uses a finite state machine (FSM) with five states:**

s_Idle: Initial state, waiting for start bit

s_RX_Start_Bit: Start bit detected, waiting for middle of start bit

s_RX_Data_Bits: Receiving data bits

s_RX_Stop_Bit: Receiving stop bit

s_Cleanup: Final state, preparing for next reception

Signals

**The architecture uses several signals:**

r_SM_Main: Current state of the FSM

r_Clk_Count: Clock counter for timing

r_Bit_Index: Bit index for receiving data bits

r_RX_Byte: Received byte signal (8 bits)

r_RX_DV: Data valid signal

Process

**The p_UART_RX process describes the behavior of the FSM:**

s_Idle: Wait for start bit, reset counters and bit index.

s_RX_Start_Bit: Check middle of start bit, if low, transition to s_RX_Data_Bits.

s_RX_Data_Bits: Receive data bits, increment clock counter and bit index.

s_RX_Stop_Bit: Receive stop bit, wait for stop bit to finish.

s_Cleanup: Prepare for next reception, reset signals.

**Output Assignments**

The output signals o_RX_DV and o_RX_Byte are assigned the values of r_RX_DV and r_RX_Byte, respectively.

In summary, this VHDL code implements a UART receiver that detects the start bit, receives data bits, and checks the stop bit to ensure valid data reception.
