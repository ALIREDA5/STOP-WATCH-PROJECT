# STOP-WATCH-PROJECT

## Description

This project implements a versatile Stop Watch system using an ATmega32 Microcontroller with the following specifications:

1. **Microcontroller:** ATmega32 with a 8 MHz clock frequency.
2. **Timer Configuration:** Timer0 is configured in CTC (Clear Timer on Compare Match) mode to count the Stop Watch time.
3. **LCD:** To dispaly counting.
4. **Keypad:** for Time Adjustment
5. **Port Configuration:** The keypad is connected to  PORTC - and the last four pins in PORTA, PINB0,PINB1,PINB3 are used for LCD Output - button for interrupts on PINB2,PIND2,PIND3 - buzzer on PIND0  .
6. **Start:** The Stop Watch counting starts automatically when power is connected to the MCU.
7. **Reset:** External Interrupt INT0, triggered by a rising edge, is used to pause the Stop Watch time.
8. **Pause:** External Interrupt INT1, triggered by a rising edge, is used to resume the Stop Watch.
9. **Resume:** External Interrupt INT2, triggered by a rising edge, is used to reset the Stop Watch.
10. **Buzzer Alarm:** In countdown mode, if the time reaches zero, a buzzer alarm will sound.

## Hardware Setup

### Components Required:

- ATmega32 Microcontroller
- LCD
- Keypad
- NPN BJT Transistors
- Push Buttons (for Reset, Pause, Resume)
- Buzzer (for alarm)
- Resistors and Capacitors (as required)
- Breadboard or PCB for Circuit Assembly
- Power Supply (5V)

### Wiring Instructions:

- Connect the ATmega32 pins according to your schematic.
- Wire LCD.
- Connect Keypad to PORTC.
- Configure external interrupts INT0, INT1, and INT2 as described in the project specifications.
- Connect a buzzer to a suitable pin (e.g., PBx) to sound the alarm when the countdown reaches zero.

## Simulation

The project was tested and simulated using Proteus Design Suite. The simulation allowed for a comprehensive evaluation of the circuit and code behavior before deploying it on the hardware.

## Usage

1. Connect the hardware components according to the wiring instructions.
2. Power up the system.
3. The Stop Watch will start counting as soon as power is connected.
4. Use the external push buttons as follows:
   - INT0 (Falling Edge): Reset the Stop Watch time.
   - INT1 (Rising Edge): Pause the Stop Watch.
   - INT2 (Falling Edge): Resume the Stop Watch.
5.  when the time reaches zero, the buzzer alarm will sound.
