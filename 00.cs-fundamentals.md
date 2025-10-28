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

## 5. Storage - The Long-Term Keeper

### 5.1. Introduction to Storage

- Storage is where data is kept permanently.
- It is non-volatile, meaning data stays even when power is off.
- Common types: HDD (Hard Disk Drive), SSD (Solid State Drive).
- Modern systems often use SSDs for speed and HDDs for large capacity.
- NVMe (Non-Volatile Memory Express) SSDs connect via PCIe for even faster speeds.

### 5.2. Types of Storage

- **HDD (Hard Disk Drive)**:
  - Uses spinning disks and read/write heads.
  - Slower but cheaper per GB.
- **SSD (Solid State Drive)**:
  - Uses flash memory (no moving parts).
  - Faster and more durable but more expensive.
- **NVMe SSD**:
  - Modern, uses PCIe lanes (direct CPU connection).
  - Extremely fast data transfer rates (up to 7000 MB/s).
- **Optical Drives**:
  - Use lasers to read/write data on CDs/DVDs.
- **External Storage**:
  - USB flash drives, external HDDs/SSDs for portability.

### 5.3. Storage Interfaces

- **SATA (Serial ATA)**:
  - Common interface for HDDs and SSDs.
  - Max speed ~600 MB/s.
- **NVMe (Non-Volatile Memory Express)**:
  - High-speed interface for SSDs using PCIe.
  - Max speed several GB/s.

## 6. Bus System - The Communication Highway

### 6.1. Introduction to Bus System

- A bus in a computer system is a communication pathway that connects different components of a computer (like CPU, memory, and input/output devices) so they can exchange data and signals efficiently.
- It is like a highway inside the computer- data and control signals travel between CPU, RAM, storage, etc.

### 6.2. Types of Buses

- **Data Bus**:
  - Carries actual data between components.
  - Width (e.g., 32-bit, 64-bit) determines how much data can be transferred at once.
- **Address Bus**:
  - Carries memory addresses from CPU to memory.
  - Width determines maximum addressable memory (e.g., 32-bit = 4GB, 64-bit = 16EB).
- **Control Bus**:
  - Carries control signals (read/write, interrupt requests) to coordinate operations.

### 6.3. Bus Architecture

- **Front-Side Bus (FSB)**:
  - Connects CPU ↔ Memory Controller (Northbridge).
  - Carries data, addresses, and control signals.
  - Modern CPUs have integrated memory controllers, so the traditional FSB is mostly replaced.

- **Back-Side Bus (BSB)**:
  - Used for CPU ↔ Cache (L3) communication.
  - Very fast and private to the CPU.

- **System Bus**:
  - Connects main memory, CPU, and I/O controllers.
  - Replaced in newer systems by point-to-point connections like Intel’s QuickPath Interconnect (QPI) or AMD’s Infinity Fabric.

- **Expansion Buses**:
  - Used to connect external or peripheral devices to the system.
  - Examples:
    - PCI Express (PCIe) → connects GPU, SSD, Wi-Fi cards, etc. (very fast).
    - USB → universal connection for peripherals (keyboard, mouse, storage).
    - SATA / NVMe → for storage devices (HDDs, SSDs).

### 6.4. Bus Speed and Performance

- Bus speed (measured in MHz or GHz) affects how fast data can be transferred.
- Wider buses (more bits) can transfer more data simultaneously.
- Modern systems use high-speed buses like PCIe for graphics cards and NVMe SSDs.

### 6.5. Data Flow via Bus System

- Let’s see how buses work together when user opens a file on the PC:
  - CPU sends a request over the control bus → “Read file data from storage.”
  - Address bus tells where the data is stored (RAM or SSD address).
  - Data bus transfers the actual bytes of the file.
  - PCIe bus might be used if the file is on an SSD.
  - The data finally reaches the CPU cache and is displayed to you.

### 6.6. Modern Advancements in Bus Systems

- Modern computer architectures focus on speed and parallelism:
  - Point-to-Point links (like QPI, HyperTransport, Infinity Fabric) replaced shared buses.
  - PCIe 5.0 / 6.0: Extremely high bandwidth for GPUs and SSDs.
  - NVLink (NVIDIA): Ultra-fast GPU-GPU communication.
  - USB4 / Thunderbolt 4: Unified high-speed I/O bus for external devices.
- These advancements ensure that data flows quickly and efficiently between components, minimizing bottlenecks and maximizing performance.

### 6.7. Summary

| Bus Type | Connects | Purpose | Example Technology |
| - | - | - | - |
| Data Bus | CPU ↔ Memory | Data transfer | DDR5 memory bus |
| Address Bus | CPU → Memory/I/O | Memory addressing | Memory mapping |
| Control Bus | CPU → All components | Control signals | Read/Write, Interrupt |
| PCIe Bus | CPU ↔ GPU/SSD | High-speed expansion | PCIe 5.0 |
| USB Bus | CPU ↔ External devices | Peripheral connection | USB4 / Thunderbolt 4 |

## 7. I/O Devices - The Interaction Points

### 7.1. Introduction to I/O Devices

- Input Devices:
  - Used to provide data to the computer.
  - Examples: Keyboard, Mouse, Microphone, Scanner.

- Output Devices:
  - Used to show processed data.
  - Examples: Monitor, Printer, Speaker.
