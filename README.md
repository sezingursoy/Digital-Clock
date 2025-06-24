# Digital-Clock
This project implements a simple digital clock using Verilog HDL. The design displays time in hours and minutes, and supports reset and pause/resume functionalities. It is ideal for simulation or FPGA-based digital design practice.

Overview
This project implements a fully functional digital clock using Verilog Hardware Description Language. The clock is capable of displaying time, resetting, and pausing/resuming the counting operation. It features input via keypad and displays output on a 7-segment LED display.

Features
Time Display (HH:MM:SS) using 6-digit 7-segment display

Reset functionality to set time back to 00:00:00

Pause / Resume capability with user input

Mode selection via control unit (Set Clock Mode, Set Alarm Mode, Display Mode)

Keypad Interface for user input (0–9, MODE, ENTER, ESC, RESET, etc.)

System Components
⌛ clock_divider_embedded
Generates a 1 Hz clock signal from a higher-frequency base clock input for timekeeping.

🕹️ CONTROL_UNIT
Handles user interaction logic. Determines current mode (e.g., setting time vs. running clock), and processes buttons like MODE, RESET, ENTER.

⏱️ clock_counter_embedded
Implements second, minute, and hour counters. Counts from 00:00:00 to 23:59:59 and wraps accordingly.

⌨️ keyboard_controller_mode
Manages keypad input. Detects numeric keys and control keys (ESC, MODE, RESET, etc.) and provides synchronized code output for further processing.

🧮 Display System
Segments the time into 6 outputs for seven-segment display: HH:MM:SS format. Multiplexed via a controller for efficient hardware usage.

Visual Overview
Project Schematic Examples (see /img/ or docs/ folder for full-resolution):

