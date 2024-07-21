# Car_Basic_Functionality

## Software & Hardware
This project is done on a 68HC12/MC9S12 microcontroller using the CodeWarrior IDE.

# Project Overview
This project demonstrates a comprehensive understanding and application of the 68HC12/MC9S12 microcontroller through the design and implementation of a software system mimicking basic car functionalities. The project integrates various hardware peripherals and a user-friendly interface to simulate the operation of a car, including features like an LCD display, speaker, switches, LEDs, and more.

# Introduction
## Purpose
The purpose of this capstone project is to encapsulate the knowledge and skills acquired over the semester in working with the 68HC12/MC9S12 microcontroller. The project aims to create a software system with hardware components that replicate basic car functionalities, leveraging the microcontroller's various peripherals.

## Assumptions Made
Hardware components (LCD, speaker, switches, LEDs, potentiometer) are reliable.
Users are competent in understanding and following the system interface.
Users input commands based on LCD instructions.
Users understand basic car functionalities and restrictions (e.g., some functions are unavailable when the car is off).
# Design
## Peripherals

The project utilizes the following peripherals with the 68HC12/MC9S12 microcontroller:

Dipswitches (control drive mode, gear, and AC speed)
LEDs (display car state and act as head/taillights)
Pushbutton (ignition switch)
Hex Keypad (user input)
LCD (display instructions and car status)
Stepper Motor (simulates tire speed)
DC Motor (simulates AC system)
Speaker (tones for pin entry and alarm)
Potentiometer
IRQ Button (alarm state activation)
Software Implementation
# Description
The software is designed to transition naturally between different car states, adhering to logical car operations. It starts in main.asm, and upon correct pin entry, it moves to main_menu.asm, where various functionalities are managed.

# Error Handling and Fail-Safe Techniques
Restricted user input based on current state (e.g., only keypad and LCD are active during pin entry).
Incorrect pin entry leads to alarm state after three attempts.
Program remains idle if no input is provided when expected.

# Additions to Project
Start-up LED animation
Three pin attempts with visual indication on LEDs
Specific tones for correct/incorrect pin entries
Encrypted pin entry display
Hazard lights and turn signals
Celsius to Fahrenheit conversion
12-hour clock format

# Project Status
## Working Portions
All functionalities of the car system are operational.

## Not Working Portions
None reported.

# Conclusion
This project successfully demonstrates the practical application of the 68HC12/MC9S12 microcontroller, integrating various peripherals to simulate car functionalities. It reflects the skills and knowledge gained throughout the course, including assembly instructions, peripheral integration, and error handling techniques.

# Discussion & Suggestions for Improvement
Future improvements could include:

Implementing a tachometer controlled by the potentiometer and DC motor
Integrating additional peripherals like a gyroscope
Using a larger LCD screen for enhanced usability
# Appendix I: User Manual
## Starting the System
The program starts with an LED animation and an "Enter the Pin" prompt on the LCD.
Enter the pin using the keypad. You have three attempts, indicated by LEDs 0-2. If all attempts are used, the system enters the alarm state.
## Main Menu
Upon correct pin entry, the main menu displays time and available actions.
When the car is off, only the turn-on function and going back are available.
Turn on the car using the pushbutton. The main dashboard shows gear, drive mode, and speed.
## Controlling the Car
Drive Mode: Switch 0 (0: Normal, 1: Sport)
Gear: Switch 1 (0: Drive, 1: Reverse)
AC Speed: Switch 7 (0: Slow, 1: Fast) or control via keypad
Turn Signals: Press A for right, 0 for left
Hazard Lights and Temperature Conversion: Access further options in the main menu
