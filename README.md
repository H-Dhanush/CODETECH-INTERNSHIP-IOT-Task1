# CODETECH-INTERNSHIP-IOT-Task1
**Name:** Dhanush H <br>
**Company:** CODETECH IT SOLUTIONS <br>
**ID:** CT08DS1824 <br>
**Domain:** Internet of Things <br>
**Mentor:** Mohammed Muzammil Ahmed <br>


## Overview of the Project

### Project: Weather Montioring Station using ESP32 with DHT11 Sensor and Thingspeak

### Objective

The primary objective of the program is to periodically read temperature and humidity data from a DHT11 sensor, calculate the heat index, and transmit these values to a ThingSpeak channel for monitoring and analysis.

### Key Activities

**Initialize Serial Communication:**
   - Sets up a serial connection for debugging and monitoring outputs using `Serial.begin(115200)`.

**Configure WiFi Mode:**
   - Sets the ESP32 to connect to an existing WiFi network using `WiFi.mode(WIFI_STA)`.

**Start ThingSpeak Communication:**
   - Initializes the connection to ThingSpeak for data uploads with `ThingSpeak.begin(client)`.

**Initialize DHT Sensor:**
   - Prepares the DHT11 sensor for reading temperature and humidity using `dht.begin()`.

**Check WiFi Connection:**
   - Verifies and attempts to reconnect to WiFi if the connection is lost using `WiFi.status()`.

**Read Sensor Data:**
   - Retrieves temperature and humidity from the DHT11 sensor using `dht.readHumidity()` and `dht.readTemperature()`.

**Calculate Heat Index:**
   - Computes the perceived temperature based on humidity and temperature using `dht.computeHeatIndex()`.

**Print Data to Serial Monitor:**
   - Outputs the sensor readings and computed heat index to the serial monitor for debugging with `Serial.print()`.

**Upload Data to ThingSpeak:**
   - Sends the sensor readings to a ThingSpeak channel using `ThingSpeak.writeFields()`.

**Update Timer:**
    - Resets the timer to control the interval between data transmissions using `lastTime = millis()`.

### Technologies Used

**ESP32**:
   - A microcontroller with integrated WiFi and Bluetooth, used for IoT applications.

**DHT11 Sensor**:
   - A digital sensor that measures temperature and humidity.

**WiFi Library (WiFi.h)**:
   - Enables the ESP32 to connect to WiFi networks.

**ThingSpeak Library (ThingSpeak.h)**:
   - Facilitates sending data to the ThingSpeak cloud service for storage and visualization.

**DHT Library (DHT.h)**:
   - Provides functions to interact with DHT sensors, like reading temperature and humidity.

**Serial Communication**:
   - Used for debugging by sending data to a connected computer via the serial port.

**Arduino IDE**:
   - The integrated development environment used to write and upload code to the ESP32.

**C++ Programming Language**:
   - The language used to write the program for the ESP32.

**ThingSpeak**:
   - An IoT cloud platform for aggregating, visualizing, and analyzing live data streams.

### Hardware and Software Required

● ESP32 <br>
● DHT22 (Humidity+Temperature) <br>
● 10K Resistor - 1 Qty <br>
● Breadboard <br>
● Jumper wires <br>
● USB cable for Programming(ESP32) <br>
● Arduino IDE <br>
● Thingspeak account <br>

### Steps to do this project:

1. Before starting this installation procedure, make sure you have the latest version of the Arduino IDE installed in your computer. If you don’t, uninstall it and install it again. Otherwise, it may not work.

2. For installing ESP32 in Arduino IDE go to the Arduino IDE in that go to **File->Prefernces**

3. In that enter **https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json** into the "Additional Board Manager URLs" field and click "OK" button.

4. Open the Boards Manager. Go to **Tools > Board > Boards Manager**

5. Search for **ESP32** and press install button for the **ESP32 by Espressif Systems.**

6. That's it. It should be **ESP32 Library** is installed after a few seconds

7. Go to **Tools > Manage Libraries > Library Manager** search for **DHT** on the search box and install the DHT library from Adafruit.

8. After installing the DHT Library from Adafruit, type **Adafruit Unified Sensor** in the search box. Scroll all the way down to find the library and install it.

9. To send Sensor readings to ThingSpeak, we'll use the ThingSpeak-Arduino Library. You can install this library through the Arduino Library manager. Go to **Sketch > Include Library > Manage Libraries...** and search for **"ThingSpeak"** in the library manager install the thingspeak library by Mathworks.

10. To use Thingspeak, you must sign in with your existing Mathworks account or create a new one. Non-commercial users may use ThingSpeak for free. Free accounts offer limits on certain functionality. Commercial users are eligible for a time-limited free evaluation. To get full access to the MATLAB analysis features on ThingSpeak, login to the ThingSpeak using the email address associated with your university or organization. To send data faster to ThingSpeak or to send more data from more devices, consider the **paid license options** for commercial, academic, home and student usage.

11. Go to **My Channels > press New Channel > Create Name > Create fields based on your needs > Select Save Channel** your channel is created in that copy paste the **Channel Id** and **Write API key**, as this API keys enable you to write data to a channel or read data from a channel. API keys are auto-generated when you create a new channel.

12. Our work is done.

### Circuit Diagram

![image](https://github.com/H-Dhanush/CODETECH-INTERNSHIP-IOT-Task1/assets/167459628/31074f9d-4207-41e2-9e1e-be4cc3a4eb41)

### Output in Serail Monitor

![image](https://github.com/H-Dhanush/CODETECH-INTERNSHIP-IOT-Task1/assets/167459628/1d3f23ea-c37e-4540-86ad-ebab651e06bb)

### Output in ThingSpeak

![image](https://github.com/H-Dhanush/CODETECH-INTERNSHIP-IOT-Task1/assets/167459628/2e45f144-4980-4f08-bfdb-e0d507aed5dc)

### Conclusion
This project successfully demonstrates how to integrate the ESP32 microcontroller with a DHT11 sensor and the ThingSpeak cloud service for real-time environmental monitoring. By leveraging WiFi connectivity and cloud-based data logging, the system provides an efficient solution for various IoT applications. The concise code structure and use of libraries make it adaptable for a wide range of projects. With minor adjustments, it can be tailored to specific use cases, from home automation to industrial monitoring.




