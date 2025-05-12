# 8-Bit Breadboard Computer Project

## Introduction

Welcome to the repository for my 8-bit breadboard computer project. This project aims to build a functional 8-bit computer from basic logic gates and ICs on breadboards, following the inspirational design by Ben Eater.

**Project Goals:**
- Gain a fundamental, hands-on understanding of low-level computing concepts, including *CPU architecture*, *instruction set design*, *memory addressing*, *control logic*, and the *fetch-decode-execute cycle*.
- Develop practical skills in digital circuit design, troubleshooting electronic circuits, and interpreting datasheets.
- Create comprehensive documentation detailing our design choices, build process, schematics, microcode, and challenges encountered, serving as a learning resource for ourselves and others.

**Based on:** [Ben Eater's 8-bit Computer Project](https://eater.net/8bit)

## Modules

This section details the individual components of our 8-bit computer. Each module was built and tested individually before system integration.

### 1. Clock Module
- **Purpose:** Generates timing signals for the entire computer, supports variable speed, single-stepping, and halting.
- **Schematic:** 
- **Build Log & Notes:** 
- **Status:**

### 2. Register A
- **Purpose:** An 8-bit general-purpose register used for temporary storage and ALU input.
- **Schematic:** 
- **Build Log & Notes:**
- **Status:**

### 3. Register B
- **Purpose:** An 8-bit general-purpose register, primarily used as the second input to the ALU.
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 4. Arithmetic Logic Unit (ALU)
- **Purpose:** Performs arithmetic (addition, subtraction) and logical operations on data from Registers A and B. Sets status flags (Zero, Carry).
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 5. RAM Module
- **Purpose:** Stores program instructions and data (e.g., 16 bytes using 74LS189 or larger static RAM). Includes the Memory Address Register (MAR).
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 6. Program Counter (PC)
- **Purpose:** Holds the memory address of the next instruction to be fetched. Can be incremented or loaded (for jumps).
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 7. Output Register & Display
- **Purpose:** Latches data from the bus to be displayed, typically on 7-segment LEDs.
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 8. Instruction Register (IR)
- **Purpose:** Holds the opcode of the current instruction being executed.
- **Schematic:**
- **Build Log & Notes:**
- **Status:**

### 9. Control Logic
- **Purpose:** Decodes the instruction in the IR and orchestrates the control signals for all other modules during each step (T-state) of the instruction cycle. Implemented using EEPROMs (microcode).
- **Schematic:**
- **Microcode:**
- **Build Log & Notes:**
- **Status:**

## System Integration

- **Bus:**
- **Final System Schematic:**
- **Integration Notes:**

## Instruction Set Architecture (ISA)

| Opcode (Binary) | Mnemonic | Description                       |
| :-------------- | :------- | :-------------------------------- |
| `0000 0000`     | NOP      | No Operation                      |
| `0001 xxxx`     | LDA      | Load Register A from RAM address `xxxx` |
| `0010 xxxx`     | LDB      | Load Register B from RAM address `xxxx` |
| `0011 xxxx`     | STA      | Store Register A to RAM address `xxxx`  |
| `0100 0000`     | ADD      | Add Register A + Register B, store in A |
| `0101 0000`     | SUB      | Subtract Register B from Register A, store in A |
| `0110 0000`     | OUT      | Output value in Register A to display |
| `0111 xxxx`     | JMP      | Jump to RAM address `xxxx`        |
| `1000 xxxx`     | JC       | Jump if Carry flag is set         |
| `1001 xxxx`     | JZ       | Jump if Zero flag is set          |
| `1111 0000`     | HLT      | Halt the clock                    |
| *(Add/modify instructions as defined by your team)* |          |                                   |

## Control Logic & Microcode

//

## Challenges & Future Work

* **Challenges Encountered:** 
* **Potential Future Enhancements:**

## License

This project is licensed under the [MIT License](LICENSE).