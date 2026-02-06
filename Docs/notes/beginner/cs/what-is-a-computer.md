# What is a Computer?

## Summary
A computer is a machine that takes input, processes it according to instructions, stores data, and produces output.
Most computers share the same fundamental architecture: computation (CPU), memory (RAM), storage (SSD/HDD), and input/output devices.
Understanding these components helps you reason about performance, debugging, and how software interacts with hardware.

## Prerequisites
- None

## Core Concepts

### Input → Process → Output
- **Input:** data enters the system (keyboard, mouse, files, network)
- **Process:** instructions execute on the CPU
- **Output:** results leave the system (screen, files, network)

### CPU (Central Processing Unit)
- Executes instructions
- Performance depends on cores, clock speed, cache, and workload type

### Memory (RAM)
- Fast, temporary storage
- Cleared when power is lost
- Insufficient RAM leads to swapping and slowdowns

### Storage (SSD/HDD)
- Persistent data storage
- SSDs are faster than HDDs for most workloads

### Input/Output (I/O)
- Communication paths between components
- Disk, network, USB, display all count as I/O

## Commands / Code

Check system information on Linux:

```bash
uname -a
lscpu
free -h
lsblk
