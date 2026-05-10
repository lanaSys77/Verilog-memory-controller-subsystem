# Verilog-Based Memory Controller Subsystem

## RTL Design & Verification Project

A complete RTL hardware design and verification project implementing a simplified memory controller subsystem using Verilog HDL.

The system connects a CPU model with a synchronous 1K×16 memory through an FSM-based memory controller supporting:

* Read/Write transactions
* Simultaneous read/write arbitration
* Fixed-latency operations
* Verification testbenches
* Full system integration

---

# System Architecture

The following diagram illustrates the communication between the CPU, Memory Controller, and Memory subsystem.

<p align="center">
  <img src="./Images/Block%20diagram%20of%20the%20system.png" width="850"/>
</p>

The controller handles:

* Request scheduling
* Read/Write arbitration
* Fixed service latency
* CPU-memory synchronization
* Pending read handling

---

# Core Design Features

## RTL Design

* FSM-based architecture
* Synchronous memory interface
* Ready/Valid handshake protocol
* One-cycle memory strobes
* Two-cycle service latency

## Verification

* Self-checking testbenches
* Timing verification
* Pulse-width validation
* Concurrent read/write testing
* Data correctness validation

## Arbitration Logic

If READ and WRITE requests arrive simultaneously:

* WRITE operation executes first
* READ request is stored temporarily
* READ executes immediately after WRITE completion

---

# FSM States

| State | Function                           |
| ----- | ---------------------------------- |
| IDLE  | Waiting for incoming requests      |
| WRITE | Executing memory write transaction |
| READ  | Executing memory read transaction  |

---

# Project Structure

```bash
Verilog-memory-controller-subsystem/
│
├── Images/
│   ├── Block diagram of the system.png
│   ├── Memory controller simulation.png
│   └── Complete system simulation.png
│
├── AdvDiditProject1220785.pdf
├── Advancedc.txt
└── README.md
```

---

# Memory Controller Simulation

The waveform below demonstrates:

* FSM transitions
* Memory write operations
* Read requests
* Ready/Valid signaling
* Write completion pulse behavior

<p align="center">
  <img src="./Images/Memory%20controller%20simulation.png" width="1000"/>
</p>

---

# Full System Simulation

The integrated system simulation verifies:

* CPU-controller interaction
* Memory transactions
* Read-after-write correctness
* Simultaneous read/write handling
* Transaction ordering

<p align="center">
  <img src="./Images/Complete%20system%20simulation.png" width="1000"/>
</p>

---

# Verification Scenarios

The verification environment checks:

* Correct write operations
* Correct read operations
* Read-after-write functionality
* Simultaneous RW arbitration
* Fixed transaction latency
* One-cycle pulse widths
* Proper FSM sequencing

---

# Technologies Used

| Category           | Technology              |
| ------------------ | ----------------------- |
| HDL                | Verilog                 |
| Design Methodology | RTL Design              |
| Architecture       | FSM                     |
| Verification       | Self-Checking Testbench |
| Domain             | Digital Systems Design  |

---

# Key Concepts

* RTL Hardware Design
* FSM Design
* CPU-Memory Interface
* Memory Arbitration
* Timing Verification
* Digital System Integration
* Hardware Verification
* Verilog HDL

---

# Learning Outcomes

Through this project, I gained hands-on experience in:

* RTL development
* FSM implementation
* Hardware verification
* Timing analysis
* System-level integration
* CPU-memory communication
* Digital architecture design

---

# Author

## Lana Ayed Sayes

Computer Engineering Student
Birzeit University
