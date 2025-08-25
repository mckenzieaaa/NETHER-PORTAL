# Nether-Portal
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

## dengdai.ino
#include <Adafruit_NeoPixel.h>
#define PIN        6
#define NUMPIXELS 120
Adafruit_NeoPixel pixels(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);
#define DELAYVAL 50

int lightPin = A0
void setup() {
}
pinMode(lightPin, INPUT);
Serial.begin(9600);
#if defined(__AVR_ATtiny85__) && (F_CPU == 16000000)
  clock_prescale_set(clock_div_1);
#endif
pixels.begin();

void loop() {
  int lightState = analogRead(lightPin);
if (lightState > 500){}
  delay(500);
  for(int i = 0; i < NUMPIXELS; i++;){
    pixels.setPixelColor(i,pixels.Color(3,289,135));
    pixels.show();
    delay(DELAYVAL);
    pixels.setPixelColor(i,pixels.Color(0,0,0));
    pixels.show();
    delay(DELAYVAL);
  }
}

## main.toe
<img width="1552" height="906" alt="part3" src="https://github.com/user-attachments/assets/8b863518-0493-4982-aa87-b7ec4d8c3db3" />
<img width="1552" height="906" alt="part2" src="https://github.com/user-attachments/assets/5b73c06a-6cce-4ddf-8522-6c758281804a" />
<img width="1552" height="906" alt="part1" src="https://github.com/user-attachments/assets/02561f18-0578-42f5-94dc-2e80294e7aa2" />

