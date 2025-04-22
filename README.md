# Floor Cleaning Robot

**Welcome** to the **Floor Cleaning Robot** project, developed during the **Design Workshop** at **Vidyashilp University, Bangalore**. This repository contains the source code, documentation, and resources for a **Bluetooth-controlled robotic prototype** designed to **vacuum** and **mop floors**, making household cleaning efficient and user-friendly.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Testing and Results](#testing-and-results)
- [Limitations and Future Improvements](#limitations-and-future-improvements)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Overview
The **Floor Cleaning Robot** is a prototype aimed at **automating household cleaning tasks**. It combines **vacuuming** and **mopping** functionalities, controlled remotely via a **Bluetooth-enabled device**. Built with affordable components like the **Arduino UNO** and **DC motors**, it offers a cost-effective solution for the domestic robotics market.

**Team Members:**
- Ayush Kumar
- Ahmed Nooruddin Mulla
- Priyanshu Bhargav

**Date:** December 15, 2023

## Features
- **Bluetooth Control**: Navigate and switch cleaning modes using a smartphone or computer.
- **Dual Functionality**: Vacuums dust/debris and mops wet surfaces.
- **Cost-Effective Design**: Utilizes affordable, accessible components.
- **Portable**: Powered by a 9V battery for easy mobility.
- **Customizable**: Open-source code supports modifications for specific needs.

## Hardware Requirements
- **Arduino UNO**
- **Bluetooth Module (HC-05)**
- **12V DC Motors (x2)** for navigation
- **Arduino Motor Driver (L298N)**
- **9V Battery**
- **1.5V Motor** for mopping
- **Chassis and Wheels**
- **Vacuum Module**
- **Mop Attachment**

## Software Requirements
- **Arduino IDE**: For uploading code to the Arduino UNO.
- **Bluetooth Terminal App**: For sending commands (e.g., Bluetooth Serial Controller for Android).
- **Operating System**: Windows, macOS, or Linux for development.

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/username/floor-cleaning-robot.git

2. **Assemble Hardware**:
   - Mount DC motors to the chassis and wheels.
   - Connect motors to the L298N motor driver.
   - Interface the Arduino UNO with the motor driver and HC-05 Bluetooth module.
   - Attach the vacuum module and 1.5V mop motor.
   - Power the system with a 9V battery.

3. **Install Arduino IDE**:
   - Download and install from [arduino.cc](https://www.arduino.cc/).
   - Install the **SoftwareSerial** library if not included.

4. **Upload Code**:
   - Open `floor_cleaning_robot.ino` in the Arduino IDE.
   - Connect the Arduino UNO via USB.
   - Upload the code to the Arduino.

5. **Pair Bluetooth**:
   - Power on the robot and pair the HC-05 module with your device (default password: `1234` or `0000`).
   - Use a Bluetooth terminal app to send commands.

## Usage
1. **Power On**: Activate the robot and ensure the Bluetooth module is operational.
2. **Connect via App**: Use a Bluetooth terminal app to connect to the HC-05 module.
3. **Send Commands**:
   - `F`: Move forward
   - `B`: Move backward
   - `L`: Turn left
   - `R`: Turn right
   - `M`: Start mopping
   - `V`: Start vacuuming
   - `S`: Stop all operations
4. **Cleaning**: Navigate the robot to clean desired areas, switching between vacuum and mop modes.
5. **Power Off**: Stop the robot and disconnect the battery when finished.

**Example Command Sequence**:
- `F`: Move forward.
- `M`: Activate mopping.
- `S`: Stop.

## Code Structure
- **`floor_cleaning_robot.ino`**: Main Arduino sketch for robot control.
  - Manages Bluetooth communication.
  - Controls motors for navigation and mopping.
  - Synchronizes vacuum operations.
- **Documentation**:
  - `docs/Floor_Cleaning_Robot_Report.md`: Detailed project report.
  - `docs/schematics/`: Wiring diagrams (to be added).

## Testing and Results
- **Navigation**: Successfully executed all directional commands via Bluetooth.
- **Cleaning**: Effectively vacuumed small debris and mopped light stains.
- **Battery Life**: Operated for **30-40 minutes** on a 9V battery.
- **Challenges**:
  - Intermittent Bluetooth connectivity issues.
  - Limited battery life and vacuum capacity for larger debris.

## Limitations and Future Improvements
### Current Limitations
- Short battery life limits continuous operation.
- Vacuum struggles with larger debris.
- Bluetooth range restricted to **~10 meters**.

### Planned Improvements
- Upgrade to a **Li-ion battery** for extended runtime.
- Integrate **ultrasonic sensors** for obstacle detection and autonomous navigation.
- Enhance the **vacuum module** for improved debris handling.
- Develop a **custom mobile app** for a seamless user experience.

## Contributing
We welcome contributions! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

Ensure your code adheres to the project's coding style and includes relevant tests.

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- **Vidyashilp University** for providing resources and support.
- **Faculty Mentors** for their guidance.
- **Open-Source Communities** for Arduino and Bluetooth libraries.

