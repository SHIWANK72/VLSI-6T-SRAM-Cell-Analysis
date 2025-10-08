# VLSI-6T-SRAM-Cell-Analysis
In-depth design and SPICE characterization of a 6-Transistor (6T) SRAM cell, analyzing stability, power, and performance.
# Design and Characterization of a 6T SRAM Cell

This repository documents the full-custom design and detailed characterization of a 6-Transistor (6T) Static Random-Access Memory (SRAM) cell. This project is a cornerstone of digital memory design, focusing on the trade-offs between stability, power consumption, and performance.

## Architecture of the 6T SRAM Cell
The standard 6T SRAM cell consists of two primary components:
1.  **Storage Latch**: Two cross-coupled CMOS inverters (four transistors) form a bistable latch to store a single bit.
2.  **Access Transistors**: Two NMOS transistors, controlled by the Word Line (WL), act as switches to connect the latch to the Bit Line (BL) and Bit Line Bar (BLB) for read and write operations.

## Project Methodology
The project was executed in two phases:

### 1. Design Phase
- **Schematic Design**: The cell was designed at the transistor level in Cadence Virtuoso. Transistor sizing (W/L ratios) was a critical parameter, carefully chosen to balance read stability and write-ability.
- **Layout Design**: A compact physical layout was created, adhering to the Design Rule Check (DRC) for the chosen technology node. Minimizing area is crucial for high-density memory arrays.

### 2. Characterization Phase
Extensive **SPICE simulations** were performed to analyze the cell's performance:
- **Static Noise Margin (SNM)**: The maximum DC noise voltage the cell can tolerate before flipping its state. This is the most critical metric for read stability. A "butterfly curve" analysis was used to measure SNM.
- **Write Margin**: Assesses the cell's ability to be written with a new value. This was determined by finding the minimum bitline voltage required to flip the cell's state.
- **Power Analysis**: Both static (leakage) and dynamic (during read/write cycles) power were measured. 

## Key Learnings
This project provided a deep, practical understanding of memory cell design, the challenges of transistor sizing, and the use of SPICE simulations to quantitatively analyze and validate a VLSI design.
