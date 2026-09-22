Secure GSM-Based Thermal Monitoring and Set-Point Control System
📌 Project Overview

The Secure GSM-Based Thermal Monitoring and Set-Point Control System is an Embedded C project designed to monitor temperature and humidity and provide remote monitoring and control through GSM communication.

The system reads temperature and humidity values from a DHT11 sensor, displays the information on an LCD, and uses GSM communication to send monitoring information. A keypad is used for user input and set-point configuration.

The system also uses I2C EEPROM for storing important data such as the password so that the stored information is retained even after power is removed.

🎯 Objectives
Monitor temperature and humidity continuously.
Display sensor readings on an LCD.
Provide GSM-based remote communication.
Allow users to configure temperature set-points.
Store password/data in non-volatile EEPROM memory.
Provide a secure user interface using keypad input.
Generate appropriate control/alert actions based on configured conditions.
🛠️ Technologies Used
Embedded C
ARM Microcontroller
Keil µVision
GSM Module
DHT11 Temperature & Humidity Sensor
I2C EEPROM
LCD
RTC
4x4 Keypad
UART Communication
I2C Communication
Interrupts
🔧 Hardware Components
ARM-based Microcontroller
GSM Module
DHT11 Sensor
16x2 LCD
I2C EEPROM
RTC Module
Matrix Keypad
Power Supply
Connecting Hardware
💻 Software
Embedded C
Keil µVision IDE
ARM Compiler
🔌 Communication Protocols UART
UART is used for serial communication between the microcontroller and GSM module.
I2C

I2C is used for communication with the EEPROM and other I2C-based devices.

📊 Main Modules

The project contains separate modules for different hardware and software functions:

main.c – Main program
dht11.c / dht11.h – DHT11 sensor interface
gsm.c / gsm.h – GSM communication
uart.c / uart.h – UART communication
i2c.c / i2c.h – I2C communication
i2c_eeprom.c / i2c_eeprom.h – EEPROM interface
lcd.c / lcd.h – LCD interface
keypad.c / keypad.h – Keypad interface
rtc.c / rtc.h – RTC interface
delay.c / delay.h – Delay functions
eint0.c – External interrupt handling
🔐 Password Storage

The system uses non-volatile EEPROM memory to store the password.

Because EEPROM is non-volatile memory, the stored password remains available even when the power supply is switched off.

The password can therefore be retained between system power cycles.

🌡️ Temperature Monitoring

The DHT11 sensor provides:

Temperature
Humidity

The microcontroller reads the sensor data and processes the values before displaying them on the LCD and using them for the configured control logic.

📱 GSM Communication

The GSM module provides remote communication capability.

UART communication is used to exchange commands and data between the microcontroller and GSM module.

🖥️ Project Flow
              ┌─────────────────┐
              │   Power ON      │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ System Init.    │
              └────────┬────────┘
                       ↓
        ┌─────────────────────────────┐
        │ Read Temperature & Humidity │
        │          DHT11              │
        └─────────────┬───────────────┘
                      ↓
              ┌─────────────────┐
              │ Process Data    │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Display on LCD  │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Check Set-Point │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ GSM Communication│
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Continue Monitor│
              └─────────────────┘


📁 Project Structure
GSM-Thermal-Monitoring-System/
│
├── README.md
│
├── src/
│   ├── main.c
│   ├── gsm.c
│   ├── gsm.h
│   ├── uart.c
│   ├── uart.h
│   ├── dht11.c
│   ├── dht11.h
│   ├── i2c.c
│   ├── i2c.h
│   ├── i2c_eeprom.c
│   ├── i2c_eeprom.h
│   ├── lcd.c
│   ├── lcd.h
│   ├── keypad.c
│   ├── keypad.h
│   ├── rtc.c
│   ├── rtc.h
│   ├── delay.c
│   └── delay.h
│
├── include/
│   ├── defines.h
│   ├── types.h
│   ├── lcd_defines.h
│   ├── keypad_defines.h
│   ├── rtc_defines.h
│   └── i2c_eeprom_defines.h
│
└── docs/
    └── project-details.md

🚀 Key Features
Real-time temperature monitoring
Humidity monitoring
GSM-based communication
UART communication
I2C EEPROM data storage
Password protection
LCD-based user interface
Keypad-based input
RTC support
Set-point configuration
Embedded C modular programming
📚 Concepts Demonstrated

This project demonstrates practical knowledge of:

Embedded C programming
Microcontroller programming
GPIO interfacing
UART
I2C
EEPROM
Interrupts
Sensor interfacing
GSM communication
LCD interfacing
Keypad interfacing
RTC
Modular firmware development
👩‍💻 Author

Selvi Kankanala

Embedded Systems Developer

Skills Demonstrated

Embedded C ARM UART I2C GSM DHT11 EEPROM RTC LCD Keypad Linux
