# NETHER-PORTAL
The code responds to mouse and keyboard inputs in TouchDesigner, triggering real-time visual changes. In TouchDesigner, these signals transform into effects such as video projection, multiplication, distortion, and immersive shifts. This highlights the Nether Portal metaphor and ensures audiences actively engage rather than passively watch.

## Demonstration
**Video Link:** https://youtu.be/a9O3xQYHBPk?si=gVv5js-mCKVKTzul
**File Link:** [NETHER PORTAL.pdf](https://github.com/user-attachments/files/21958228/NETHER.PORTAL.pdf)

## Software Used
*   **Microcontroller:** Arduino Uno
*   **Sensors:** Touch Sensor 
*   **Actuators:** WS2812B LED Strip
*   **Software:** Arduino IDE, Touch Designer

## Code Structure
dengdai.ino – Arduino sketch for handling sensor signals and sending them to the computer.
main.toe – The main TouchDesigner project, processing inputs from mouse and keyboard to generate real-time visual effects.

## How to Run
1.  Connect your Arduino Uno and upload the `dengdai.ino` sketch.
2.  Open the `main.toe` file in Touch Designer.
