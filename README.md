# Arduino Smart Parking System

This project is an Arduino-based smart parking system that automates parking management using sensors, an RFID reader, a servo motor, and an LCD display.

## Main Features

- Car detection using **infrared sensors (TCRT5000)** for 6 parking slots
- Access control via **RFID module (RC522)** for authorized vehicles
- Gate opening and closing with **servo motor (SG90)**
- Real-time parking status and available slots displayed on **16×2 LCD with I2C interface**
- "Parking Full" notification when all slots are occupied

## System Components

- Arduino Uno R3
- TCRT5000 Infrared Sensor (6 units)
- RC522 RFID Reader Module
- SG90 Servo Motor
- 16×2 LCD with I2C Module
- External Power Supply

## How It Works

1. **Entry Process**:
   - Driver presents an authorized RFID card
   - System checks for available parking slots
   - If slots are available, servo motor opens the gate
   - Infrared sensor detects vehicle entry and updates slot status

2. **Parking Monitoring**:
   - Infrared sensors continuously monitor each parking slot
   - LCD displays real-time status (E = Empty, F = Full)
   - Available slots counter updates automatically

3. **Exit Process**:
   - Infrared sensor detects vehicle at exit
   - Servo motor opens the gate for exit
   - System updates slot availability

4. **Security Features**:
   - Only authorized RFID cards allow entry
   - Prevents entry when parking is full
   - Unauthorized vehicles cannot access the parking area

## Code Structure

The system uses:
- RFID library for card authentication
- Servo library for gate control
- LiquidCrystal_I2C for display management
- Digital input reading for sensor data processing

## Project Creators

- Ali Mohammadi Seraji
- Mohammad Mehdi Kariminik

This system demonstrates practical IoT application for smart city infrastructure, combining hardware integration, sensor networks, and access control in a complete parking management solution.
