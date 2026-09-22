🔐 Secure GSM-Based Thermal Monitoring and Set-Point Control System

Embedded C | ARM7 LPC2148 | GSM | DHT11 | I²C EEPROM | LCD | Keypad


📌 Project Overview

The Secure GSM-Based Thermal Monitoring and Set-Point Control System is an Embedded C based project developed using the LPC2148 ARM7 microcontroller.

The system monitors temperature and humidity using a DHT11 sensor, displays the measured values on a 16×2 LCD, provides GSM-based communication, and allows user interaction through a 4×4 keypad.

An I²C EEPROM is used for non-volatile data storage, allowing important information such as the password and configured set-points to remain stored even after power is removed.



🎯 Objectives

Monitor temperature and humidity in real time.

Display sensor values on a 16×2 LCD.

Provide GSM-based remote communication.

Allow user input through a 4×4 keypad.

Configure temperature and humidity set-points.

Store important data in non-volatile EEPROM.

Provide password-based access.

Develop the firmware using modular Embedded C programming.


🛠️ Technologies Used

Embedded C

ARM7 / LPC2148

Keil µVision

GSM Communication

UART

I²C

DHT11

I²C EEPROM

16×2 LCD

4×4 Keypad

External Interrupt


🔧 Hardware Components

LPC2148 ARM7 Microcontroller

GSM Module

DHT11 Temperature & Humidity Sensor

16×2 LCD

I²C EEPROM

4×4 Matrix Keypad

Push Button / Switch

5V Power Supply

Connecting Wires and Supporting Components


🔌 Circuit Pin Connections

The following connections are used in the project:

<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/2834b91b-a132-4dcf-82e8-39d3534e31ae" />



🔌 Circuit Diagram



<img width="1536" height="1024" alt="Project flow" src="https://github.com/user-attachments/assets/30216205-d153-4472-9456-012c83a0fe84" />




🏗️ System Architecture


                    ┌─────────────────────┐
                    │     LPC2148 ARM7    │
                    │   Microcontroller   │
                    └─────────┬───────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
        ▼                     ▼                     ▼
  
      DHT11               16×2 LCD             4×4 Keypad
      Sensor               Display               Input   

        │
        │
        ▼
    Temperature
        & 
      Humidity
     
        │
        └──────────────────┐
                           ▼
                 
                    ┌─────────────┐
                    │ GSM Module  │
                    │Communication│
                    └─────────────┘

                    ┌─────────────┐
                    │ I²C EEPROM  │
                    │ Data Storage│
                    └─────────────┘

                    ┌─────────────┐
                    │   Switch    │
                    │   P1.15     │
                    └─────────────┘



🔄 Project Working Flow Diagram

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/97390daa-b395-40bc-8062-ca2c37b307a6" />



🔐 EEPROM Data Storage

The project uses I²C EEPROM as non-volatile memory.

Important information such as the password and configured set-point values can be stored in EEPROM so that the data is retained even when the system is powered OFF.


🌡️ Temperature & Humidity Monitoring

The DHT11 sensor is used to measure:

Temperature

Humidity

The LPC2148 reads the sensor data through the DHT11 data line connected to P0.4.
The measured values can then be displayed on the LCD and compared with the configured set-points.


📱 GSM Communication

The GSM module provides remote communication capability.

The UART interface is used between the LPC2148 and GSM module:

LPC2148 P0.1  → GSM TX connection

LPC2148 P0.0  → GSM RX connection

The GSM module can be used for sending monitoring or alert information.


⌨️ Keypad Interface

A 4×4 matrix keypad is connected to:

P1.16 – P1.23

The keypad is used for:

Password entry

Menu selection

Set-point configuration

User input


🔘 Switch / Interrupt

A push button or switch is connected to:

P1.15

It can be used for menu or interrupt-based user interaction.


💻 Software

Development Environment

Keil µVision

ARM Compiler

Embedded C

Programming Concepts

Embedded C

GPIO

UART

I²C

Interrupts

Sensor interfacing

LCD interfacing

Keypad interfacing

EEPROM data storage

GSM communication

Modular firmware development


📁 Project Structure

GSM-Thermal-Monitoring-System/
│

├── README.md

├── main.c

├── dht11.c


├── dht11.h

├── gsm.c

├── gsm.h

├── uart.c

├── uart.h

├── lcd.c

├── lcd.h

├── keypad.c

├── keypad.h

├── i2c.c

├── i2c.h

├── eeprom.c

├── eeprom.h

├── delay.c

├── delay.h

│

├── circuit_diagram.png

├── project_flow.png

└── hardware_setup.jpg

⭐ Key Features

   Real-time temperature monitoring
   
    Humidity monitoring
   
    GSM-based communication
   
    Password protection
   
    Non-volatile EEPROM storage
   
    LCD display
   
    4×4 keypad interface
   
    Switch/interrupt interface
   
    Modular Embedded C firmware
   
    ARM7 LPC2148 microcontroller

   
📚 Skills Demonstrated:

Embedded C |  ARM7 |  LPC2148 | UART |  I²C |  GSM |  DHT11 |  EEPROM |  LCD |  Keypad |
Interrupts |  Keil µVision.

👩‍💻 Author

Kankanala  Selvi

Embedded Systems Developer

📌 Project Documentation

The repository includes the source code, circuit diagram, project flow diagram, hardware information, and software implementation details for this Embedded Systems project.
