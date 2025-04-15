# Wood Dryer ESP32

A project for an automated wood dryer with internet control based on the ESP32 Wroom CH340. The system measures temperature, controls the heater, and logs data. 

## Features

- Temperature measurement using a Pt100 sensor via MAX31865
- Heater control via relay
- Web interface for monitoring and controlling the drying process
- Preparation for data logging and automatic mode regulation

## Project Structure

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
