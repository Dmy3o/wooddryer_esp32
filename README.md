# Wood Dryer ESP32

A project for an automated wood dryer with internet control based on the ESP32 Wroom CH340. The system measures temperature, controls the heater, and logs data. 

## Features

- Temperature measurement using a Pt100 sensor via MAX31865
- Heater control via relay
- Web interface for monitoring and controlling the drying process
- Preparation for data logging and automatic mode regulation

## Project Structure

## System Overview

The following table lists all main components used in the dryer system:

| No. | Component                         | Description                                                         | Quantity | Notes                                 |
|-----|-----------------------------------|---------------------------------------------------------------------|----------|----------------------------------------|
| 1   | Air temperature sensor            | Measures ambient temperature in the dryer (e.g. DS18B20)           | 1        | Mounted in the drying chamber          |
| 2   | Air humidity sensor               | Measures ambient humidity (e.g. DHT22 or AM2320)                   | 1        | Placed near the temperature sensor     |
| 3   | Psychrometric sensors (PT100)     | Wet and dry bulb thermometers for relative humidity calculation    | 2        | Each connected via MAX31865            |
| 4   | Wood core temperature sensor      | Measures internal temperature of the lumber (e.g. PT100)           | 1        | Inserted into the center of the board  |
| 5   | Fan                               | Air circulation inside the dryer                                   | 1–2      | Controlled via relay or PWM            |
| 6   | Heating element                   | Heats the air inside the dryer                                     | 1        | Controlled via relay or SSR            |
| 7   | ESP32 controller                  | Central logic and Wi-Fi control unit                               | 1        | Core of the system                     |
| 8   | MAX31865                          | ADC interface for PT100 sensors via SPI                            | 2        | One per PT100                          |
| 9   | Web interface                     | UI for monitoring and control via browser                          | 1        | Hosted on the ESP32                    |

## Getting Started

1. Install all necessary libraries in the Arduino IDE:
   - `Adafruit MAX31865`
   - `WiFi` (built into ESP32)
   - `AsyncWebServer` (optional)

2. Connect the Pt100 sensor via MAX31865 according to the schematic (see `hardware/`)

3. Upload the sketch from the `firmware/` folder

## Web Interface

A simple interface is planned for:
- Displaying temperature readings
- Starting/stopping the drying process
- Event log

## Author

Developer: [Dmy3o](https://github.com/Dmy3o)

Collaboration is welcome — feel free to contribute to the repository!

---

## License

This project is licensed under the **Apache 2.0 License**.
