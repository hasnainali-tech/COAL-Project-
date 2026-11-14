# COAL-Project

# Restaurant Management System using Assembly Language

**EL-2003 Computer Organization and Assembly Language (COAL) Lab: Project Proposal**
National University of Computer and Emerging Sciences (FAST-NUCES), Karachi Campus | Fall 2026

| | |
| --- | --- |
| **Group ID** | BCS-3E-01 |
| **Lab Section** | BCS-3E |
| **Lab Instructor** | Sir Abdullah Shaikh |
| **Submission Date** | 15 October 2026 |

## Group Members

| S. No. | Name | Roll Number | Role |
| --- | --- | --- | --- |
| 1 | Muhammad Ahmad | 25K-0587 | Group Leader |
| 2 | Muhammad Shaheer Ismail Khan | 25K-0676 | Member |
| 3 | Hasnain Ali | 25K-0841 | Member |

## Abstract

This project designs and implements a console-based Restaurant Management System in x86 Assembly Language using the Irvine32 library in Visual Studio. It provides restaurant administration, table seating reservations, order processing, and automated receipt generation. Menu item names and prices are stored in parallel arrays, table availability in two-dimensional arrays, and administrator login is verified with the `CMPSB` string instruction. `MUL` and `DIV` compute bill totals and tax, while `SHR` applies instant promotional discounts. Modular execution uses stack frames, `PROC` directives, and `INVOKE`, with a recursive routine for loyalty reward points and inline assembly for core computational logic. Work is divided among team members across console menu layout, memory offset management, array manipulation, and arithmetic algorithms. The final program displays real-time menu choices, manages inventory limits, and calculates final balances within a command-line interface.

## Introduction and Problem Statement

A restaurant must coordinate several activities at the same time: showing the menu, seating customers, taking orders, keeping track of stock, and producing an accurate bill. When these tasks are handled manually, mistakes in table allocation, stock counts and bill calculation are common and slow down service.

This project addresses the problem with a console-based Restaurant Management System that brings restaurant administration, table seating reservations, order processing and automated receipt generation into one interactive program. Assembly Language is a good fit because each part of the system maps directly onto a low-level concept: menu data is held in parallel arrays and accessed through indirect addressing, table availability is a two-dimensional array, and billing relies on `MUL`, `DIV` and shift instructions. Implementing the system in x86 Assembly gives direct control over memory offsets and registers and builds practical experience with how these operations work at machine level.

## Objectives

- Build a functional restaurant management terminal application using x86 Assembly Language
- Apply indirect addressing, parallel arrays, and two-dimensional arrays for inventory and seating management
- Implement multiplication, division, extended addition, and bitwise shift instructions for billing and discounts
- Demonstrate modular structure through procedures, stack frames, `INVOKE` directives, and recursive routines
- Gain practical experience with memory handling and inline assembly within Visual Studio

## Scope of the Project

**The project WILL include:**

- Administrator login verified with a string comparison (`CMPSB`)
- Display of menu items and prices stored in parallel arrays
- Table seating reservation using a two-dimensional availability array
- Order processing with inventory (stock) limits
- Receipt generation with bill total, tax and promotional discount, and loyalty reward points calculated by a recursive procedure
- A keyboard-driven console interface built with the Irvine32 library

**The project will NOT include (out of scope):**

- A graphical user interface, networking, or online ordering and payment processing
- Permanent storage of records between program runs (data is held in memory while the program runs)
- Multi-user or multi-terminal operation

## Proposed Features / Modules

| No. | Feature / Module | Description |
| --- | --- | --- |
| 1 | Admin Login | Verifies the administrator by comparing the entered string with the stored one using `CMPSB`. |
| 2 | Main Menu Interface | Console menu built with Irvine32 procedures that shows the choices and reads the user's selection. |
| 3 | Menu and Pricing | Stores item names and prices in parallel arrays and displays them using indirect addressing. |
| 4 | Table Reservation | Tracks table availability in a two-dimensional array and reserves seats. |
| 5 | Order Processing and Inventory | Records customer orders, enforces stock limits and updates quantities. |
| 6 | Billing, Tax and Discount | Calculates totals and tax with `MUL`, `DIV` and extended addition; applies instant discounts with `SHR`. |
| 7 | Receipt Generation | Displays the final receipt with the total, tax, discount and final balance. |

## Assembly Language Concepts to be Used

| Concept | Where it is used |
| --- | --- |
| Registers, data movement and indirect addressing | Moving data and accessing item, price and stock arrays through offsets. |
| Arrays and addressing modes | Parallel arrays for menu names and prices; two-dimensional array for table availability. |
| String instructions (`CMPSB`) | Administrator login verification. |
| Arithmetic instructions (`MUL`, `DIV`, extended addition) | Bill totals, tax calculation and large sums. |
| Conditional jumps and loops | Main menu loop, input validation and stock-limit checks. |
| Procedures, stack frames, `PROC` and `INVOKE` | Modular routines for each feature, with parameters passed through the stack. |
| Recursion | Calculation of loyalty reward points. |
| Irvine32 library procedures | Console input and output, such as `WriteString`, `ReadString`, `ReadInt` and `WriteDec`. |
| Inline assembly | Core computational logic integrated within Visual Studio. |

## Tools and Environment

- **Assembler:** MASM
- **IDE:** Microsoft Visual Studio
- **Library:** Irvine32 (x86 console application)

## Work Division

| Member | Responsibilities |
| --- | --- |
| Muhammad Ahmad (Group Leader) | Memory offset management and array manipulation: parallel arrays, two-dimensional table array, stock limits and order processing. |
| Shaheer Ismail Khan | Console menu layout and main program flow, administrator login (`CMPSB`), input validation and module integration. |
| Hasnain Ali | Arithmetic algorithm implementation: billing with `MUL` and `DIV`, tax, discount, recursive loyalty points and receipt generation. |

All members take part in testing, debugging and the final report.

## Tentative Timeline

| Week / Dates | Task | Responsible |
| --- | --- | --- |
| 16 Oct – 25 Oct | Finalize design; set up Visual Studio and Irvine32; implement main menu layout, admin login and data arrays (menu, prices, tables, stock). | Muhammad Ahmad, Shaheer Ismail Khan |
| 26 Oct – 8 Nov | Implement table reservation, order processing with stock limits, and billing with tax and `SHR` discount. | Shaheer Ismail Khan, Hasnain Ali |
| 9 Nov – 18 Nov | Implement recursive loyalty points and receipt generation; integrate inline assembly and all modules. | All members |
| 19 Nov – 22 Nov | Testing, debugging and final report. | All members |

## Expected Outcome

A fully working Restaurant Management System capable of taking customer orders, reserving seats, updating stock limits, and calculating final receipts with tax and discounts, validated through executable console operations.

The program runs in a console window. After logging in as administrator, the user enters a number from the main menu to view the menu, reserve a table, place an order or print a receipt, and the screen updates immediately with availability, stock and totals.

## References

- K. R. Irvine, *Assembly Language for x86 Processors*, 8th ed., Pearson, 2019.
