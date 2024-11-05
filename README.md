# AWECG-Monitor

This is the Arduino code to create the BLE server to capture the ECG signal and communicate with the app AWECG.

The sample rate is 250Hz and the resolution is 12 bits. The signal is amplified by an AD8232, and the microcontroller is an ESP32.

## How to use
1. Download the code and open it with the PlatformIO IDE.
2. Connect the ESP32 to the computer.
3. Upload the code to the ESP32.
4. Open the app AWECG and connect to the ESP32.
5. Enjoy!

## How to connect the AD8232
The AD8232 gets the ECG signal to get I derivation. It's necessary to connect the AD8232 to the ESP32 with the following pins:

| AD8232 | ESP32 |
|--------|-------|
| GND    | GND   |
| 3.3v   | 3.3V  |
| OUTPUT | IO 32 |
| LO+    | NC    |
| LO-    | NC    |
| SDN    | IO 14 |

## How to connect the Wake-up button
The wake-up button is used to wake up the ESP32 from deep sleep mode. The Button is connected to the ESP32 using a pull-down resistor. The ESP32 is woken up when the button is pressed. The button is connected to the ESP32 with the IO 12.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact Information

- **Alejandro Pulido Saravia**: [https://www.linkedin.com/in/pulidosaravia/](https://www.linkedin.com/in/pulidosaravia/)
- **Email**: [pulidosaravia@gmail.com](mailto:pulidosaravia@gmail.com)

Electronic Engineering  
Bucaramanga, Colombia  
2023
