You can view the detailed design of the project on Tinkercad using this link:
[Smart Blind Stick – Tinkercad](https://www.tinkercad.com/things/aYw4zb50xun-smart-blind-stick?sharecode=buESlD5yPGCEs2KCdzq6VA1mmRrWrLD1N79N59o3g6w)



This algorithm implements a priority-driven sensing and alert system using ultrasonic sensors, temperature monitoring, and light detection. It begins by initializing serial communication, allocating memory for multiple sensor–actuator pairs, configuring pin modes, and preparing all peripherals for operation.

The main loop follows a strict priority model.
Highest priority: Obstacle detection using ultrasonic sensors, where each measured distance triggers or deactivates its corresponding actuator and buzzer alert based on proximity.
Moderate priority: Temperature monitoring, which reads and converts analog values to Celsius and triggers a buzzer warning when the value goes outside a defined safe range.
Lower priority: Light level monitoring, which checks ambient brightness and activates alerts when levels fall below a set threshold.

Each cycle ends with a short delay to ensure stable sampling. Memory cleanup is supported for safe shutdown.
This approach ensures critical obstacle alerts are handled first, while environmental monitoring tasks run reliably in the background.


