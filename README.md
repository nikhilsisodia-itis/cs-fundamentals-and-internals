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
