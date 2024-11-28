# Smart Irrigation System

## **Overview**
The **Smart Irrigation System** is an automated solution designed to monitor soil moisture levels and optimize water usage for irrigation. It uses a soil moisture sensor to determine when plants require water and controls a water pump to irrigate as needed. The system also includes a user-friendly interface, real-time clock functionality, and custom volume dispensing for precise water management.

This project aims to provide an efficient and smart way to manage water resources, ensuring plants receive the right amount of water without waste.

---

## **Features**
1. **Automated Soil Moisture Monitoring**:
   - Measures soil moisture levels using a capacitive soil moisture sensor.
   - Activates a water pump automatically when the soil is dry.

2. **Custom Volume Dispensing**:
   - Allows users to manually input a specific volume of water (in milliliters) to be dispensed.
   - Dispensing time is calculated based on the pump's flow rate (120 L/h).

3. **Real-Time Clock Integration**:
   - Displays the current time and date on an OLED screen.
   - Saves the last recorded time and date to EEPROM for persistence across power cycles.

4. **Dynamic OLED User Interface**:
   - Displays real-time sensor readings (voltage and soil condition).
   - Provides interactive menus for selecting irrigation modes and viewing system information.

5. **Visual Feedback**:
   - Displays smiley/sad faces based on soil conditions (e.g., wet/dry soil).
   - Countdown timer for dispensing water ensures precise control.

6. **Keypad Control**:
   - Easy-to-use 4x3 matrix keypad for user input.
   - Buttons allow for navigating menus, confirming selections, and clearing inputs.

---

## **Components Used**
1. **Hardware**:
   - **Arduino Uno R3**: Microcontroller for handling logic and control.
   - **Capacitive Soil Moisture Sensor**: Detects soil moisture levels.
   - **Soil Moisture Sensor Interface Module**: Converts sensor readings to analog and digital signals.
   - **OLED Display (128x64)**: Displays sensor data, menus, and system feedback.
   - **4x3 Keypad**: Provides user input for selecting options and entering custom values.
   - **Relay Module**: Controls the water pump based on sensor data.
   - **Water Pump**: Dispenses water as required for irrigation.
   - **EEPROM**: Stores clock data for persistence across power resets.

2. **Power Supply**:
   - 5V power supply for the Arduino and peripherals.

---

## **How It Works**
1. **Soil Monitoring**:
   - The soil moisture probe measures the conductivity of the soil.
   - The interface module converts this to analog and digital signals for the Arduino to process.
   - Based on the readings:
     - **Wet Soil**: The system turns off the water pump.
     - **Dry Soil**: The system activates the water pump.

2. **Custom Water Dispensing**:
   - The user can enter a custom water volume using the keypad.
   - The system calculates the time required to dispense the specified volume based on the pump's flow rate (120 L/h).

3. **User Interface**:
   - The OLED screen displays real-time data, including:
     - Current soil moisture levels (in volts).
     - Smiley/sad faces based on soil conditions.
     - Time and date.
   - Menus allow the user to select preset volumes, view system status, or dispense custom water volumes.

4. **Clock Functionality**:
   - The system maintains real-time clock functionality.
   - Saves and retrieves the time and date from EEPROM to ensure data persistence.

5. **Adjustable Sensitivity**:
   - The soil moisture sensor's threshold can be adjusted using the potentiometer on the interface module.

---

## **Features of the Code**
- **Efficient Modular Design**:
  - Functions are structured for specific tasks, such as displaying menus, updating the clock, and handling sensor input.
- **Robust Error Handling**:
  - Prevents invalid inputs and handles scenarios where inputs exceed acceptable ranges.
- **Scalability**:
  - Designed to support additional sensors or features, such as remote monitoring or multi-zone irrigation.

---

## **Necessary Information**
1. **Calibrating the Sensor**:
   - Adjust the potentiometer on the sensor interface module to calibrate the soil moisture threshold.
   - Observe the LED on the module for changes in the digital output (DO).

2. **Pump Flow Rate**:
   - Ensure the pump flow rate matches the assumed 120 L/h for accurate custom dispensing.

3. **Connections**:
   - **Keypad**: Connect rows to pins 6-9, columns to pins 10, 11, 13.
   - **Soil Sensor**:
     - Analog Output (AO) to A0.
     - Digital Output (DO) to D5.
   - **Relay Module**: Connect control pin to D4.

4. **Project Limitations**:
   - The soil sensor's sensitivity to water might vary based on environmental conditions or wear over time.
   - Ensure good wiring connections to prevent errors during operation.

---

## **Acknowledgments**
This project was completed as part of a semester project for an embedded systems course that I am taking in Khalifa University, Abu Dhabi, UAE. We would like to thank our lecturer for the guidance and feedback provided throughout the development of this system.

---
