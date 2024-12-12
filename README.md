# Assignment
LED Blinking with Tactile Switch on STM32G070RB

Project Description

This project demonstrates how to control an LED connected to an STM32G070RB Nucleo board using a tactile switch. The LED operates in different modes based on the number of button presses, cycling through the following states:

1st Press: LED blinks at 0.5 Hz.
2nd Press: LED blinks at 1 Hz.
3rd Press: LED blinks at 2 Hz.
4th Press: LED turns off.
5th Press: Resets to the 1st state, repeating the cycle.
Additionally, the microcontroller enters a low-power mode when the LED is off to optimize power consumption.

Features

Tactile switch input handling with debouncing.
LED blinking at different frequencies.
Power optimization using low-power modes.
Cycle-based state management.
Hardware Requirements
STM32G070RB Nucleo board.
1 x Tactile switch.
1 x LED.
1 x Resistor (330 OHM for LED).
Breadboard and jumper wires.

Circuit Diagram

Connections:

Tactile Switch:
One leg to PC13 (GPIO input).
Other leg to GND.

LED:

Anode (longer leg) to PA5 (GPIO output).
Cathode (shorter leg) to GND through a 330 OHM resistor.

Software Requirements

STM32CubeIDE: To write and upload the code to the microcontroller.
STM32CubeMX (optional): To configure peripherals if needed.

How to Run the Code

Clone this repository to your local machine:

git clone https://github.com/amrutheshtk/Assignment.git

Open the project in STM32CubeIDE.
Build the project and upload it to the STM32G070RB board.
Connect the hardware components as per the circuit diagram.

Press the tactile switch and observe the LED blinking behavior.

Code Overview

main.c: Contains the main program logic.
Configures GPIO pins for LED and switch.
Implements state transitions based on button presses.
Manages power consumption by entering low-power mode when LED is off.

Assumptions

The tactile switch is debounced using a simple delay.
GPIO PA5 is used for the LED, and PC13 is used for the switch (default configuration for Nucleo boards).
Internal pull-up resistors are enabled for the switch input.