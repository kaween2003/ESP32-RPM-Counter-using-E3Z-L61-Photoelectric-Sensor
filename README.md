📌 Project Overview
This project utilizes an ESP32 microcontroller and a generic E3Z-L61 narrow-beam photoelectric sensor to measure the RPM (Revolutions Per Minute) of a motor wheel. The measurement is achieved by reading the frequency at which a 3 cm reflective sticker passes through the sensor's infrared beam.

⚙️ Sensor Specifications (E3Z-L61 Clone)
We are using a locally sourced (Pettah) generic clone of the Omron E3Z-L61.

Type: Narrow-beam photoelectric diffuse-reflective sensor.

Operating Voltage: 12-24V DC.

Output Type: NPN Open Collector (sinks current to ground when triggered).

Operation Mode: Selectable Light-ON / Dark-ON (via physical switch).

Response Time: Typically 1 millisecond (0.001 s).

Beam Spot Diameter: Extremely narrow (ideal for small targets/stickers).

🔌 Wiring Diagram (ESP32 Integration)
Because the sensor requires 12V-24V DC but the ESP32 operates on strict 3.3V logic, the sensor cannot be directly powered by the ESP32. Furthermore, because it is an NPN Open Collector, it requires a pull-up resistor to provide a steady HIGH signal to the ESP32 when the sensor is idle.

⚠️ WARNING: Never connect a 12V source directly to an ESP32 GPIO pin. Always verify the sensor output voltage with a multimeter before connecting.
