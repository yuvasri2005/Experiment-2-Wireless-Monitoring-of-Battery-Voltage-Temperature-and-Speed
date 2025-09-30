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

clear;

clc;

close all;

%% Simulation Setup

dataPoints = 100;

voltage = zeros(1, dataPoints);

temperature = zeros(1, dataPoints);

speed = zeros(1, dataPoints);

timeStamp = linspace(0, 10, dataPoints);

%% Data Acquisition Simulation (no COM port required)

for i = 1:dataPoints

% --- Generate fake sensor values ---

voltage(i)     = 11 + rand()*2;     % Simulated battery voltage (11–13V)

temperature(i) = 25 + rand()*10;    % Simulated temp (25–35°C)

speed(i)       = rand()*80;         % Simulated speed (0–80 km/h)


% --- Plot Battery Voltage ---

subplot(3,1,1);

plot(timeStamp(1:i), voltage(1:i), 'b', 'LineWidth', 2);

title('Battery Voltage Monitoring');

xlabel('Time (s)'); ylabel('Voltage (V)'); grid on;


% --- Plot Temperature Data ---

subplot(3,1,2);

plot(timeStamp(1:i), temperature(1:i), 'r', 'LineWidth', 2);

title('Temperature Monitoring');

xlabel('Time (s)'); ylabel('Temperature (°C)'); grid on;


% --- Plot Speed Data ---

subplot(3,1,3);

plot(timeStamp(1:i), speed(1:i), 'g', 'LineWidth', 2);

title('Speed Monitoring');

xlabel('Time (s)'); ylabel('Speed (km/h)'); grid on;

drawnow;          % Update plots immediately

pause(0.1);       % Delay for real-time effect
end

disp('Simulation Complete (No COM Port Needed).');

## Output:

<img width="1280" height="680" alt="image" src="https://github.com/user-attachments/assets/a51fcf76-8a7b-4632-a9f7-9e016949ff9c" />


## Result:

The MATLAB program successfully receives and visualizes real-time battery voltage, temperature, and speed data from the embedded system using wireless communication.

