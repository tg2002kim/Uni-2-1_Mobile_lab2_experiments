ECG Measurement and Visualization via Mobile App

A Final Project for Basic Mobile Lab, Dept. of Mobile System Engineering, Dankook University


Overview
  This repository presents a project conducted as a part of Basic Mobile Lab course. The goal was to develop a mobile app that can receive and visualize ECG (Electrocardiogram) signals in real-time using an Arduino-based ECG board and Bluetooth communication. The app was developed using MIT App Inventor to allow for fast prototyping and easier UI control without native Android coding.



Project Objective
* Understand and implement serial communication between microcontroller and mobile app.

* Build an ECG acquisition system using ECG sensor + Arduino + Bluetooth module (HC-06).

* Create a real-time data visualization app using MIT App Inventor.

* Explore Bluetooth protocols (AT Commands, master/slave, SPP) and data stream management.

* Demonstrate and test the system with actual heart rate measurements.



Theoretical Background
1. ECG (Electrocardiogram)
* Measures electrical activity of the heart over time.
* Represented as a periodic waveform (P, QRS, T segments).
* Signals are weak and typically require amplification and filtering before being processed.

2. Microcontroller & Sensor Interface
* ECG sensor board transmits analog signals to Arduino Uno (ATmega328P).
* Arduino reads analog ECG input and transmits it via serial UART to Bluetooth module.
* The Bluetooth module (HC-06) is configured to communicate with mobile devices using AT commands.

3. UART & Bluetooth Communication
* ART (Universal Asynchronous Receiver/Transmitter) enables asynchronous serial data exchange.
* Data frame includes:
    * Start bit
    * Data bits (usually 8 bits)
    * Optional parity bit
    * Stop bit
* HC-06 Bluetooth module is connected via UART to the Arduino and communicates wirelessly with the smartphone app.



System Architecture

[ ECG Sensor Board ]
         |
         v
[ Arduino UNO (ATmega328P) ]
         |
   Serial UART (TX/RX)
         |
[ Bluetooth Module (HC-06) ]
         ~
     Wireless
         ~
[ Android App (MIT App Inventor) ]



Mobile App Design

Tool: MIT App Inventor
* Drag-and-drop based mobile development tool from MIT.
* Allows Bluetooth communication, real-time drawing, and simple GUI updates.

Core UI Components
* ListPicker: Connect to available Bluetooth devices
* Canvas: Draw the ECG waveform
* Labels: Display current value and voltage
* Clock: Repeatedly polls and updates display at intervals (e.g., every 100 ms)

App Logic (Simplified)
* Select Bluetooth device via ListPicker
* Connect using BluetoothClient.Connect
* Timer event triggers every 100 ms
* If connected, BluetoothClient.ReceiveText reads ECG signal string
* Value is parsed and used to:
    * Update labels
    * Draw line on canvas (real-time waveform)
* Canvas resets when it overflows width


AT Command Examples

AT           -> OK
AT+VERSION   -> HC-06 version info
AT+ADDR      -> MAC address
AT+NAME ECG01 -> Device name
AT+PSWD 1234 -> Set password
AT+BAUD8     -> Set baud rate (115200)



Project Files

File / Folder	Description
app_layout.png	Screenshot of the app's layout
final_project.pptx	Presentation of system structure, demo, and implementation details
bluetooth_commands.png	Summary of HC-06 AT command reference
ecg_data_visualization_demo.png	Real-time ECG visualization captured during test
README.md	This document



Future Improvements
* Replace MIT App Inventor with a native Android app (Kotlin or Flutter)
* Add heartbeat detection and BPM display
* Implement data logging and cloud upload (Firebase)



Acknowledgment

This work was conducted as part of "Basic Mobile Lab" (기초모바일실험) in the 2nd semester of 2024, Department of Mobile System Engineering, Dankook University.