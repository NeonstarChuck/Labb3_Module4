# Labb3_Module4

## Tilt + Sound + LCD + Buzzer Project

This Arduino project combines a tilt sensor, sound sensor (simulated with a potentiometer), 16x2 LCD display, and a buzzer to create an interactive monitoring system.

### Features

- **Tilt Detection**: Monitors tilt sensor state and displays status on LCD
- **Sound Level Monitoring**: Reads sound levels (via potentiometer) and categorizes them as:
  - QUIET (≤ 10)
  - MODERATE (11-30)
  - LOUD (> 30)
- **LCD Display**: Shows real-time tilt status and sound levels on a 16x2 LCD
- **Buzzer Alerts**: When tilt is detected, the buzzer sounds with pitch varying based on sound level:
  - QUIET: 250 Hz
  - MODERATE: 500 Hz
  - LOUD: 1000 Hz
- **Serial Debug Output**: Provides real-time sensor readings via Serial Monitor

### Hardware Components

- Arduino board (Uno/Nano/etc.)
- 16x2 LCD Display
- Tilt sensor (digital)
- Potentiometer (simulating sound sensor)
- Buzzer
- Jumper wires and breadboard

### Pin Configuration

#### LCD Connections
- RS → Pin 12
- EN → Pin 11
- D4 → Pin 5
- D5 → Pin 4
- D6 → Pin 3
- D7 → Pin 2

#### Sensors and Actuators
- Tilt Sensor → Pin 7
- Sound Sensor (Potentiometer) → A0
- Buzzer → Pin 9

### How to Use

1. Open `TiltSoundLCDBuzzer/TiltSoundLCDBuzzer.ino` in Arduino IDE
2. Connect your Arduino board and select the correct board and port
3. Upload the sketch
4. Open Serial Monitor at 9600 baud to view debug output
5. Tilt the sensor to trigger the buzzer
6. Adjust the potentiometer to change sound levels

### Operation

- **No Tilt**: Display shows "No tilt" and buzzer is silent
- **Tilt Detected**: Display shows "Tilt detected" on line 1, sound level on line 2, and buzzer sounds with pitch based on the sound level

### Serial Output Format

```
Tilt: [0/1] | Sound: [0-1023]
[Sound Level Status]
```