# Blood Glucose Tracking System

This Arduino-based system tracks blood glucose levels using a connected sensor and displays the results on an LCD screen. It connects to a designated server to fetch the latest blood glucose data and updates the display accordingly.

## Requirements

- Arduino board (e.g., ESP8266)
- Blood glucose sensor
- Wi-Fi connection
- LiquidCrystal_I2C library
- ArduinoJson library

## Setup

1. Connect the blood glucose sensor to the Arduino board.
2. Connect the Arduino board to the Wi-Fi network by updating the `ssid` and `password` variables in the code with your network credentials.
3. Ensure the LiquidCrystal_I2C and ArduinoJson libraries are installed in your Arduino IDE.
4. Upload the provided code to your Arduino board.

## Usage

- Upon startup, the system initializes and connects to the Wi-Fi network.
- It then establishes a connection with the designated server to fetch blood glucose data.
- The fetched data is displayed on the LCD screen, including blood glucose level (`BG`) and the time of the last reading (`LR`).
- The system continuously updates the display and fetches new data at regular intervals.

## Customization

- Adjust the Wi-Fi network credentials by modifying the `ssid` and `password` variables.
- Customize the server endpoint by updating the URL in the `client.connect()` function.
- Modify the display format or add additional features as needed by editing the code.

## Dependencies

- [ESP8266WiFi](https://github.com/esp8266/Arduino/tree/master/libraries/ESP8266WiFi)
- [Wire](https://www.arduino.cc/en/reference/wire)
- [LiquidCrystal_I2C](https://github.com/johnrickman/LiquidCrystal_I2C)
- [ArduinoJson](https://arduinojson.org/)
- [WiFiClientSecure](https://arduino-esp8266.readthedocs.io/en/latest/esp8266wifi/client-secure-class.html)

## Credits

- This project utilizes the ESP8266WiFi library for Wi-Fi connectivity.
- The LiquidCrystal_I2C library is used to control the LCD display.
- ArduinoJson library is employed for parsing JSON responses from the server.
