# Arduino Cooling System Project

## Overview
This project is an embedded system that monitors temperature using a TMP36 sensor and automatically activates a cooling fan when the temperature exceeds a predefined threshold. It uses an Arduino Uno, a 16x2 LCD display, and a relay-controlled fan to manage and visualize thermal conditions.

## Features
- Displays real-time temperature on LCD
- Activates fan at temperatures ≥ 79°C
- Displays warning at temperatures ≥ 93°C
- Uses serial output for debugging
- Includes visual feedback with LCD display

## Components Used
| Component                     | Quantity | Description                       |
|------------------------------|----------|-----------------------------------|
| Arduino Uno                  | 1        | Main controller                   |
| TMP36 Temperature Sensor     | 1        | Measures temperature              |
| 16x2 LCD Display (I2C)       | 1        | Displays temperature & fan status|
| Relay Module (5V)            | 1        | Controls the fan                  |
| Fan (12V)                    | 1        | Activates for cooling             |
| External Power Supply (12V)  | 1        | Powers the fan                    |
| Misc (breadboard, wires, etc)| -        | For connections                   |

## How It Works
1. TMP36 reads the ambient temperature via analog input (A0).
2. The temperature is calculated using the formula:  
   `Temp (°C) = -40 + 0.488155 * (analogRead(A0) - 20)`
3. If temperature ≥ 79°C → the fan is turned ON.
4. If temperature ≥ 93°C → LCD displays HIGH TEMP warning.
5. Otherwise, the fan is OFF.

## Schematics
![Circ](https://github.com/user-attachments/assets/f4100377-99bb-4786-bed9-b51a405648cc)

[Cooling System.pdf](https://github.com/user-attachments/files/20960956/Cooling.System.pdf)


## Source Code
The main logic is in `cooling_system.ino`.

## Author
**[Hristo Dimitrov]**  
Course Project – Embedded Systems  
[29/06/2025]

## License
This project is for educational use only.
