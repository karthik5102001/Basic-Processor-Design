
# Simple 16-bit Instruction Set Processor

## Overview
This project implements a 16-bit simple instruction set processor that supports 26 instructions. The instruction set includes:
- **Load and Store Instructions**: Transfer data between registers and memory.
- **Arithmetic Instructions**: Perform basic arithmetic operations like addition and subtraction.
- **Logical Instructions**: Bitwise operations such as AND, OR, XOR, and NOT.
- **Jump Instructions**: Control program flow with conditional and unconditional jumps.
- **Halt Instruction**: Stops processor execution.

## Processor Architecture
The processor consists of the following key components:

### 1. Control Unit
The **Control Unit** fetches instructions from **Program Memory**, decodes them, and controls the operation of other units based on the instruction type.

### 2. General-Purpose Registers
A set of registers that temporarily store data and operands for instructions.

### 3. Arithmetic Unit
The **Arithmetic Unit** performs mathematical computations such as addition, subtraction, and other arithmetic operations.

### 4. Logic Unit
The **Logic Unit** performs bitwise logical operations such as AND, OR, XOR, and NOT.

### 5. Data Memory
This block stores data that can be accessed during instruction execution (for example, variables and arrays in a program).

### 6. Program Memory
Stores the program instructions to be executed.

### 7. Instruction Register
Holds the currently fetched instruction before it is decoded by the control unit.

### 8. GPIO Interface
The processor includes an interface for General Purpose Input/Output (GPIO) using input and output buffers:
- **Input Buffer**: Captures external data from GPIO.
- **Output Buffer**: Sends processed data to external devices.

### 9. Special Function Register (SFR)
The processor includes a **Special Function Register (SFR)** that is used to store the upper 16 bits (MSB) when performing a 16-bit multiplication. Since multiplying two 16-bit numbers results in a 32-bit value, the lower 16 bits are stored in a general-purpose register, while the upper 16 bits are stored in the SFR.

## Diagram
Below is a cleaner version of the architecture diagram for better clarity:

![Processor Architecture](https://drive.google.com/file/d/1qZF9fC9Vpw6pl3C8vV6zawtxe8wwZd3i/view?usp=drive_link)

## Features
- **16-bit processing**
- **Simple and efficient design**
- **26-instruction set**
- **Supports external GPIO communication**
- **Basic memory operations with load/store**
- **Special Function Register (SFR) for 32-bit multiplication result handling**

## Usage
The processor can be used in small embedded applications, educational projects, and learning-based CPU design implementations.

---

This project provides an understanding of basic processor architecture and the integration of arithmetic, logical, and control units to execute a minimal instruction set.
