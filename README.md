### buffer-overflow-lab

## Buffer Overflow Attack Lab
# Overview
This repository contains my work for the Buffer Overflow Attack Lab, where I explored various buffer overflow vulnerabilities and exploitation techniques. The lab focuses on understanding how buffer overflows work, how they can be exploited, and the effectiveness of different protection mechanisms.

# Task 1: Understanding Shellcode

Examined 32-bit and 64-bit shellcode
Demonstrated shellcode execution by spawning shells

# Task 2: Understanding the Vulnerable Program

Analyzed buffer overflow vulnerability in stack.c
Identified key security issues (lack of bounds checking, Set-UID permissions)

# Task 3: Exploiting 32-bit Program (Level 1)

Used GDB to determine buffer and return address locations
Developed a working exploit using NOP sled technique
Successfully gained root shell through buffer overflow

# Task 4: Exploiting Unknown Buffer Size (Level 2)

Created a generalized exploit that works for any buffer size from 100-200 bytes
Implemented return address spraying at multiple offsets
Demonstrated practical attack technique for scenarios with limited information

# Task 5: 64-bit Exploitation Challenges (Level 3)

Investigated unique challenges in 64-bit exploitation
Addressed NULL byte issues in 64-bit addresses
Documented limitations and solutions for 64-bit buffer overflow attacks

# Task 6: Small Buffer Exploitation (Level 4)

Attempted exploitation of a tiny buffer (10 bytes)
Documented challenges with limited buffer space

# Task 7: Defeating dash's Countermeasure

Demonstrated dash's privilege-dropping protection
Created an improved exploit with setuid(0) to maintain privileges
Successfully circumvented shell-based security mechanisms

# Task 8: Testing Address Randomization

Enabled ASLR and tested brute-force attack method
Documented effectiveness of address randomization as a protection
Analyzed feasibility on 32-bit vs. 64-bit systems

# Task 9: Testing Protection Mechanisms

Evaluated StackGuard protection (stack canaries)
Tested non-executable stack protection
Demonstrated how modern protections effectively prevent buffer overflow attacks

# File Structure

exploit.py: Main exploit for 32-bit program (Level 1)
exploit-L2.py: Exploit for unknown buffer size (Level 2)
exploit-L3.py: Exploit attempt for 64-bit program (Level 3)
exploit-L4.py: Exploit attempt for small buffer (Level 4)
exploit-setuid.py: Exploit with setuid(0) to defeat dash's countermeasure
brute-force.sh: Script for brute-forcing address randomization
stack.c: Vulnerable program source code

# Key Learnings

Buffer overflow attack mechanics and exploitation techniques
Architectural differences between 32-bit and 64-bit exploitation
Effectiveness of various protection mechanisms:

Address Space Layout Randomization (ASLR)
StackGuard (stack canaries)
Non-executable stack (NX bit)
Shell-based privilege dropping



# Environment

Ubuntu 20.04 SEED Lab VM
GCC compiler with various protection mechanisms enabled/disabled
GDB debugger for memory analysis

# Disclaimer
This project was completed for educational purposes only. The techniques demonstrated should not be used against systems without proper authorization.
