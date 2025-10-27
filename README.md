# Computer System Fundamentals and Internals

## 1. Introduction to Computer System

### 1.1. Definition

- A computer system is a combination of hardware and software that works together to process data and perform tasks automatically.

### 1.2. Components of a Computer System

- The 4 main components of a computer system are:
  - Hardware
  - Software
  - Data
  - Users

### 1.3. Hardware- The Physical Layer

- **Input Devices**:
  - They allow the user to send data/instructions to the computer.
  - Examples: Keyboard, Mouse, Microphone, Scanner.

- **Output Devices**:
  - They show the results of processing.
  - Examples: Monitor, Printer, Speaker.

- **CPU (Central Processing Unit)**:
  - The brain of the computer.
  - It processes all instructions.
  - Has three main parts:
    - ALU (Arithmetic Logic Unit) – performs calculations and logic.
    - CU (Control Unit) – directs the flow of data.
    - Registers – small, fast storage inside CPU.

- **Memory**:
  - Stores data temporarily or permanently.
  - RAM (Random Access Memory) – temporary, volatile memory (data lost when power off).
  - Storage (SSD/HDD) – permanent, non-volatile memory (data stays when power off).

- **Motherboard**:
  - The main circuit board that connects all components so they can communicate.

- **Power Supply Unit (PSU)**:
  - Converts wall electricity into usable power for computer components.

### 1.4. Software- The Logical Layer

- **System Software**:
  - Manages hardware and provides a platform for other software.
  - Examples: Operating Systems (Windows, Linux), Utility Programs.
- **Application Software**:
  - Programs that perform specific tasks for users.
  - Examples: Word Processors, Web Browsers, Games.

### 1.5. Data

- Raw facts and figures that are processed into information.
- Data → processed by CPU/software → becomes information.
- Examples: Text files, Images, Videos, Databases.

### 1.6. Users

- People who interact with the computer system.
- Types of users:
  - End Users: Regular users who use applications.
  - System Administrators: Manage and maintain computer systems.
  - Developers: Create software applications.

### 1.7. How Hardware and Software Communicate

- User → Software (Applications) → Operating System → Drivers → Hardware
- Example (pressing a key):
  - User press “A”.
  - Keyboard hardware sends an electrical signal.
  - Keyboard driver in OS translates that signal.
  - The OS tells the application (like a text editor) — “User typed A”.
  - The app displays “A” on screen.
- Each layer translates and passes messages to the next — this is called a “stack”.

## 2. Hardware Layer (The Physical Core of the Computer System)

### 2.1 Introduction to Hardware

- Hardware is the tangible (physical) part of a computer.
- It’s everything user can touch and see — from the keyboard to the CPU chip.

### 2.2 Hardware responsibilities

- It is responsible for:
  - Input – receiving data.
  - Processing – transforming data.
  - Storage – keeping data.
  - Output – showing results.

### 2.3 Hardware Functional Blocks

- A computer’s hardware can be visualized in five main functional blocks:

```bash
Input Devices → CPU ↔ Memory ↔ Storage ↔ Output Devices
                      ↑
                     Bus System (communication link)
```

## 3. CPU - The Central Processing Unit

### 3.1. Introduction to CPU

- The CPU is the brain of your computer.
- It executes instructions, performs calculations, and controls data flow between components.

### 3.2. CPU Components and Functionality

- The CPU consists of:

  | Part | Full Form | Function | Example |
  | - | - | - | - |
  | **ALU** | Arithmetic Logic Unit. | Performs math and logical operations. | Add, subtract, compare values. |
  | **CU** | Control Unit. | Directs data movement and coordinates operations. | Tells ALU and memory what to do. |
  | **Registers** | – | Tiny, super-fast storage locations inside CPU. | Store immediate values, e.g., result of 2+3. |

### 3.3. CPU Operation Cycle

- How CPU works:
  1. Fetch: Get instruction from memory.
  2. Decode: Figure out what the instruction means.
  3. Execute: Perform the operation (math, data move, etc.).
  4. Store: Save results back to memory or registers.

### 3.4. CPU Performance Factors

- Multicore & Multithreading:
  - Core:
    - A processing unit inside a CPU chip.
    - Modern CPUs have multiple cores (e.g., 4-core, 8-core).
  - Thread:
    - A lightweight virtual CPU.
    - Each core can handle multiple threads using Hyper-Threading.
- Clock Speed:
  - Measured in GHz (gigahertz).
  - Higher clock speed = more instructions per second.
- Cache Memory:
  - Small, fast memory inside CPU.
  - Stores frequently used data for quick access.
- Instruction Set Architecture (ISA):
  - The set of instructions the CPU can understand and execute.
  - Examples: x86, ARM.

### 3.5. Types of CPUs

- CISC (Complex Instruction Set Computer):
  - Has many complex instructions.
  - Example: Intel x86 processors.
- RISC (Reduced Instruction Set Computer):
  - Has fewer, simpler instructions.
  - Example: ARM processors.

## 4. Memory - The Working Space

### 4.1. Introduction to Memory

- Memory is where data is temporarily stored while being processed.
- It is volatile, meaning data disappears when power is off.
- `sudo dmidecode -t memory` can be used on Linux to show actual RAM stick details (brand, size, speed).
- Main type: RAM (Random Access Memory).

### 4.2. Memory Hierarchy

| Level | Name | Speed | Example | Purpose |
| - | - | - | - | - |
| L1 Cache | Inside CPU | Fastest | 32KB–64KB | Immediate data |
| L2 Cache | Inside CPU | Fast | 256KB–1MB | Recent data |
| L3 Cache | Shared | Slower | 4MB–12MB | Shared by cores |
| RAM | Outside CPU | Slower | 8GB, 16GB, 32GB+ | Main working memory |
| Storage | Disk | Slowest | 512GB, 1TB, 2TB+ SSD | Long-term storage |

### 4.3. Types of Memory

- **DRAM (Dynamic RAM)**:
  - Most common type of RAM.
  - Needs constant refreshing to keep data.
- **SRAM (Static RAM)**:
  - Faster and more expensive.
  - Doesn’t need refreshing.
- **Virtual Memory**:
  - Uses part of storage (HDD/SSD) as extra RAM when physical RAM is full.
  - Slower than real RAM.

### 4.4. Data Flow in Memory

- Example: User opens a photo:
  - File is read from SSD → RAM.
  - CPU accesses the photo data in RAM.
  - CPU processes (renders) it.
  - Output sent to GPU/Monitor.
