# CS-104: Assembly Language Lesson Outline

## Resources

- Michael Scott, Programming Language Pragmatics (2009)
- MIT Open Courseware, Assembly and Computer Architecture
- [What are Assembly Languages](https://www.freecodecamp.org/news/what-are-assembly-languages/)
- [Beginning x64 Assembly Programming: From Novice to AVX Professional](https://learning.oreilly.com/library/view/beginning-x64-assembly/9781484250761/)
- [Low-Level Programming: C, Assembly, and Program Execution on Intel® 64 Architecture](https://learning.oreilly.com/library/view/low-level-programming-c/9781484224021/)

## Learning Standards
### Initial Draft, will move to the excel when finalized

- Learning Standard 1
  - There are four stages of the compilation process: Preprocessing, Compiling, Assembling, Linking
- Learning Standard 2
  - Preprocessing is first step of compilation and is used to prepare the user's code for machine code by removing comments, expand included macros, and perform and code maintenance prior to handing the file to the compiler.
- Learning Standard 3
  - Compiling is the process of taking the expanded file from the preprocessor and translating the program into assembly.
- Learning Standard 4
  - Assembling is the process of taking assembly language program and using an assembler to generate machine code.
- Learning Standard 5
  - Linking is the process of including additional objects, libraries, and source code from other locations into the code.
- Learning Standard 6
  - Assembly language is a low-level programming language used to directly correspond with machine code.
- Learning Standard 7
  - Assembly code begins with an opcode and then references memory locations or data types to operate on.
- Learning Standard 8
  - Arithmetic operations manipulate data to produce a desired result.
- Learning Standard 9
  - Memory access operations load and store information to and from registers, cache, or secondary storage locations.
- Learning Standard 10
  - Control operations change what instruction is processed next to create loops or conditional statements.
- Learning Standard 11
  - Data can be directly accessed by referencing the location that the data is stored.
- Learning Standard 12
  - Data is indirectly accessed by passing an memory address that contains another address instead of additional data for processing.
- Learning Standard 13
  - Assembly language is a near one to one equivalency to machine code, one line for assembly equals one line of machine code.

## Lesson Description

The purpose of this lesson is to give the learner a solid understanding of assembly language and the reason it is taught. It should leave the learner with a healthy knowledge of how higher level computer languages are translated and executed by the computer hardware as well as how to optimize some of your high-level code to take advantage of the way data is moved, accessed, and executed at the most basic execution.

The lesson will begin with a brief history of Assembly and why it was created before going into the reason for learning how computer code is executed so close to the hardware. A quick overview of the standard compilation process as a whole will be followed by a break down of the assembly instruction format. The learner should be able to quickly link the binary and ISA lessons to asssembly as they continue to climb the computer infrastructure hierarchy.

The next three exercises will cover some specific introductory assembly commands and what happens behind the code. The goal again is to have the student walk away with an understanding of how assembly works in the big picture, not to dive deep into a specific assembly language. 

Another short recap on the purpose and implementation of registers and a cache will be coupled with an explanation of memory addressing, both direct and indirect.

The final two exercises will focus on finishing the link between machine code and assembly. Big and Little endian will be discussed to bring those terms at least into the user's vocabulary before showing how some MIPS binary instructions, which the learner will be familiar with, direct translate over into assembly and how to do it.

## Lesson Code Description

Lesson checkpoints will serve primarily as a place to answer questions and reinforce core principles throughout the exercise. No large programs will be created for this lesson.

## Exercise Overview

- Introduction and Why
- Assembly Benefits
- Compilation Process
- Assembly Code Format
- Arithmetic Operations
- Memory Access Operations
- Control Flow Operations (Branches / Jumps)
- Registers / Cache
- Memory Addressing (Direct/Indirect)
- Big Endian / Little Endian
- Translation to/from Binary
- Summary

Link to x86 or MIPS documentation for further reading throughout lesson.

## Exercises In-Depth

#### Introduction and Why (Text / Image)

- NARRATIVE
  - What is Assembly?
    - Human-readable (barely) machine code
  - Original Purpose
    - The Computer Hamburger (The next ingredient)
  - Getting "Under The Hood" to make better decisions
- CHECKPOINTS
  - Move to the next exercise
- ARTWORK: Hamburger Analogy

#### Modern Assembly Purpose/Benefits (Text / Image)

- NARRATIVE
  - Assembly in the Industry
  - Cost of Code
    - Data Structures
    - Memory Access
    - Etc
  - Performance Enhancement (Micro vs Macro Improvements)
    - The goal is not to master assembly, but understand how it works because your specific processor determines the specific assembly language variation to learn.
- CHECKPOINTS
  - Move to the next exercise
- ARTWORK: Three Computers, each screen showing x86, ARM, or MIPS.

#### Compilation Process (Text / Code / Console) OR (Text / Image)

- NARRATIVE
  - Preprocessing
  - Compiling
  - Assembly
    - 1:1 Assembly to Binary
  - Linking
- CHECKPOINTS
  - Click run to see the machine code outputs of the assembly instructions
- ARTWORK: None

#### Assembly Code Format (Text / Code / Console)

- NARRATIVE
 - Breakdown a basic Assembly Instruction
   - OPCODEs, memory locations, system codes
- CHECKPOINTS
 - Answer questions:
   - First part of an instruction is what?
   - How is data stored/accessed?
   - Etc
- ARTWORK: None

#### Arithmetic Operations (Text / Code / Console)

- NARRATIVE
 - Explain Add/Sub/Mult/Div &  AND/OR/NOT/Shifts
- CHECKPOINTS
 - Answer questions
- ARTWORK: NONE

#### Memory Access Operations (Text / Code / Console)

- NARRATIVE
 - Explain Loading and Store Operations
- CHECKPOINTS
 - Answer Questions
- ARTWORK: NONE

#### Control Flow Operations: Branches, Jumps & Loops (Text / Code / Console)

- NARRATIVE
 - Explain Jumps, Branches, and Loops
 - Caller / Callee & Returns
- CHECKPOINTS
 - Have sample assembly code in editor, follow control flow through program
   - Start here, what comes next?
   - And then where based on a conditional branch?
   - Who is the original caller? What are we returning? Etc
- ARTWORK: NONE

#### Registers / Cache

- NARRATIVE
 - Why use them
 - Move things close to the processor, operate on them, shove them back.
 - When pulling from memory, we should be doing other operations (pipelining)
   - Fetching from memory = several hundred cycles
   - Fetching from registers / cache = typical one cycle
- CHECKPOINTS
 - None
- ARTWORK: CPU Diagram from ISA lesson OR Data Bus GIF

#### Memory Addressing: Direct and Indirect (Text / Code / Console)

- NARRATIVE
 - Explain direct and indirect addressing
 - Explaion how it's performed in Assembly
 - Briefly touch on hexadecimal because addresses are typical in this format
   - Maybe link to this lesson that is currently being developed right now by Kim Pries for some other course: [Binary and Bases](https://author.codecademy.com/content-items/6ebf93a62ca5d6ea3ee5545eed086427/drafts/60c77cd7bc9ce50023237d72)
- CHECKPOINTS
 - Answer questions about addressing
- ARTWORK: None

#### Big Endian &  Little Endian (Text / Code / Console)

- NARRATIVE
 - Binary Storage Techniques
 - Explain Big Endian and Use Cases
 - Explain Little Endian and Use Cases
- CHECKPOINTS
 - Answer: Is this big or little endian?
- ARTWORK: None

#### Translation to/from Binary (Text / Code / Console)

- NARRATIVE
 - Use MIPS demonstrate how the instructions translate into each other: Assembly to Binary
- CHECKPOINTS
 - Given an OPCODE Table:
   - Translate an assembly instruction to binary
   - Translate a binary instruction to assembly
- ARTWORK: None

#### Summary
- NARRATIVE
  - Summarize Assembly Purpose
  - Summarize Instruction Format
  - Summarize Basic Instruction Types
- CHECKPOINTS
  - None
- ARTWORK: Hamburger Analogy
