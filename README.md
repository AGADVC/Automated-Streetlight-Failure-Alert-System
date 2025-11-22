# Automated-Streetlight-Failure-Alert-System
This project uses an ESP32, LDR sensor, and GPS module to automatically detect streetlight failures. When continuous darkness is detected, the system verifies GPS coordinates and sends an email alert to authorities with the exact location. It improves maintenance efficiency and supports smart‑city monitoring.

# Smart Streetlight Fault Detection System
Overview: 
The Smart Streetlight Fault Detection System is an IoT‑based project designed to automatically detect malfunctioning streetlights using an ESP32 microcontroller, an LDR sensor, and a GPS module. Many cities rely on manual inspection to find streetlights that stop working, which is inefficient and often leads to delays in repairs. This project eliminates that problem by continuously monitoring light intensity and sending real‑time alerts when a streetlight is detected as faulty.

By integrating sensor data, GPS tracking, and WiFi‑based email notifications, the system provides a modern, reliable, and scalable solution for smart‑city infrastructure. It ensures that issues are identified and reported immediately, reducing maintenance costs and improving public safety.

How It Works: 
At the core of the system is an ESP32 board, which reads data from an LDR (Light Dependent Resistor) to measure ambient light. In normal conditions, a functioning streetlight illuminates the area at night, and the LDR registers relatively low values. If the streetlight fails, the LDR will detect continuous darkness.

The system uses a timer to prevent false triggers—only if the LDR senses darkness for a specified period will the system assume the streetlight is broken. Temporary shadows or noise in readings will not activate the alert.

Once the darkness time threshold is met, the GPS module (such as a NEO‑6M) provides accurate latitude and longitude coordinates. This ensures that the location of the faulty streetlight is precisely identified, even in areas with many streetlights.

After obtaining valid GPS data, the ESP32 uses the ESP Mail Client library to send an automated email to the designated authority. This email includes the detected LDR value, the exact GPS coordinates, and the timestamp. Maintenance teams can then quickly locate and fix the damaged streetlight.

Features: 
Automatic Fault Detection: Continuously checks light levels using an LDR sensor.
Smart Timer Logic: Prevents false alarms by using a darkness‑duration threshold.
GPS Integration: Sends accurate coordinates for easy location tracking.
WiFi‑Enabled Alerts: Emails are sent in real time via an SMTP server.
Scalable Design: Can be deployed across multiple streetlights.
Low‑Cost IoT Solution: Uses inexpensive hardware that's easy to set up.

Hardware Required: 
ESP32 Development Board
LDR + 10k ohm resistor
NEO‑6M GPS module
Jumper wires, breadboard
WiFi connection
Power supply or battery
Software Requirements
Arduino IDE
ESP32 Board Manager
TinyGPS++ Library
ESP Mail Client
WiFi.h (comes with ESP32 package)

Applications: 
This system is ideal for:
  Smart‑city automation
  Public utility maintenance
  Road safety improvements
  Large‑scale IoT infrastructure
  Energy monitoring networks

Conclusion: 
The Smart Streetlight Fault Detection System represents a practical and effective use of IoT technology in urban infrastructure. By automatically detecting faults and providing real‑time alerts with exact GPS coordinates, the system significantly reduces the time required for repairs and ensures safer, well‑lit streets. Its efficient design, scalability, and accuracy make it a valuable component in the development of smart cities.
