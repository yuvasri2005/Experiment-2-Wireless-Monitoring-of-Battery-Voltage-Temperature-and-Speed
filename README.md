# Experiment-2-Wireless-Monitoring-of-Battery-Voltage-Temperature-and-Speed

## Aim:

To design and implement a MATLAB-based system to monitor parameters such as battery voltage, temperature, and vehicle speed, and wirelessly transmit the data to a central monitoring station.
 
## Theory:
1. Importance of Monitoring Parameters in Electric Vehicles (EVs)
•	Battery Voltage: Ensures efficient power distribution and prevents over-discharge.
•	Temperature: Protects the battery and motor from overheating.
•	Speed: Helps maintain optimal performance and energy consumption.
2. Wireless Data Transmission
•	Wi-Fi (ESP8266/ESP32), Bluetooth (HC-05), or ZigBee (XBee) can be used to send sensor data.
•	The central monitoring station receives data and displays it using MATLAB.
 
## Procedure:
1.	Sensor Setup:
o	Use sensors like LM35 (temperature), voltage dividers (battery voltage), and Hall-effect sensors (speed).
o	Connect them to an Arduino/ESP32/Raspberry Pi for data acquisition.
2.	Wireless Communication:
o	Use Wi-Fi (ESP8266/ESP32) or Bluetooth (HC-05) to send data to a central monitoring station.
3.	MATLAB Data Processing:
o	Read the incoming serial data.
o	Parse and store voltage, temperature, and speed values.
o	Display the data using real-time plots.
 
## Program:




## Output:


 
## Result:
The MATLAB program successfully receives and visualizes real-time battery voltage, temperature, and speed data from the embedded system using wireless communication.

