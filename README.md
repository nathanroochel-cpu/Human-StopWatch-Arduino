Human Stopwatch
An Arduino stopwatch controlled by a single push button. Press to start, press again to stop. Time shows live on the LCD while it's running.
How it works
On startup the LCD says "Press Start". When you press the button it clears and shows "Go!" then starts counting up in seconds. Press it again and it freezes on "Final:" with your time. Uses debounce filtering so the button reads cleanly.
Hardware
Arduino Uno
16x2 LCD
1 push button
Potentiometer (LCD contrast)
Breadboard + jumper wires
No pull-down resistor needed for the button — the sketch uses INPUT_PULLUP, so just wire one leg to pin 2 and the other to GND.
Wiring
LCD → Arduino
```
RS  → Pin 7
E   → Pin 8
D4  → Pin 9
D5  → Pin 10
D6  → Pin 11
D7  → Pin 12
VDD → 5V
VSS → GND
V0  → Potentiometer wiper
A   → 5V
K   → GND
```
Button → Arduino
```
One leg → Pin 2
Other   → GND
```
Setup
Open `HumanStopwatch.ino` in the Arduino IDE
Select Board: Arduino Uno and your port
Upload
Wire it up and power via USB
Library
Uses the built-in `LiquidCrystal` library — no extra installs needed.
