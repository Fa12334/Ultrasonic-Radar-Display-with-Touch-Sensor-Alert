t
# Ultrasonic Radar System with Touch Sensors and Display

## Overview
This project implements an ultrasonic radar system using an ST7735 display, an HC-SR04 ultrasonic sensor, a servo motor, touch sensors, and LEDs. The system scans for objects, displays their position on the screen, and activates buzzers and LEDs when a touch sensor is triggered.

## Features
- Ultrasonic distance measurement
- Radar-like display visualization
- Servo motor for scanning
- Touch sensors to detect interaction
- LED and buzzer alerts based on distance and touch input

## Components Used
- **Microcontroller**: Arduino (or compatible board)
- **Ultrasonic Sensor**: HC-SR04
- **Display**: ST7735 (Ucglib library used)
- **Servo Motor**: Generic 9g servo
- **Touch Sensors**: Two digital touch sensors
- **LEDs**: Two LEDs (left and right indicators)
- **Buzzers**: Two buzzers for alarm indication

## Pin Configuration
| Component          | Pin Number |
|-------------------|------------|
| Ultrasonic Trig   | 6          |
| Ultrasonic Echo   | 5          |
| Servo Signal      | 7          |
| Display CS        | 10         |
| Display DC        | 9          |
| Display Reset     | 8          |
| LED Right        | 3          |
| LED Left         | 2          |
| Touch Sensor Right | 4         |
| Touch Sensor Left  | 5         |
| Buzzer Right      | 12         |
| Buzzer Left      | 14         |

## Code Explanation
1. **Setup**:
   - Initializes the display, ultrasonic sensor, servo, touch sensors, LEDs, and buzzers.
   - Sets the pin modes appropriately.
   - Starts serial communication for debugging.

2. **Loop**:
   - Reads the touch sensor states.
   - Controls the buzzers based on touch input.
   - Moves the servo in a sweeping motion.
   - Calculates distance using the ultrasonic sensor.
   - Displays the radar visualization on the ST7735 display.
   - Turns LEDs on or off based on detected objects.

3. **Functions**:
   - `calculateDistance()`: Measures the distance using the HC-SR04 sensor.
   - `fix()`: Draws the radar outline on the display.

## Installation
1. Install **Ucglib** and **Servo** libraries in the Arduino IDE.
2. Connect the components as per the pin configuration.
3. Upload the code to the Arduino board.
4. Open the Serial Monitor (9600 baud) to debug distance readings.

## Usage
- The servo sweeps to detect objects using the ultrasonic sensor.
- Detected objects appear on the radar display.
- If an object is close to the sensor, the corresponding LED and buzzer will activate.
- If a touch sensor is triggered, the system alerts with buzzers.

## Future Enhancements
- Improve distance accuracy by filtering noise.
- Implement real-time data logging.
- Add Bluetooth or WiFi connectivity for remote monitoring.

## License
This project is open-source and can be modified or distributed under the MIT License.
