Floor Cleaning Robot

Welcome to the Floor Cleaning Robot project, developed as part of the Design Workshop at Vidyashilp University, Bangalore. This repository contains the source code, documentation, and resources for a Bluetooth-controlled robotic prototype designed to vacuum and mop floors, making domestic cleaning more efficient and user-friendly.

Table of Contents





Project Overview



Features



Hardware Requirements



Software Requirements



Installation



Usage



Code Structure



Testing and Results



Limitations and Future Improvements



Contributing



License



Acknowledgments

Project Overview

The Floor Cleaning Robot is a prototype aimed at automating household cleaning tasks. It integrates vacuuming and mopping functionalities, controlled remotely via a Bluetooth-enabled device. The project leverages affordable components like the Arduino UNO and DC motors to provide a cost-effective solution for the growing domestic robotics market.

Team Members:





Ayush Kumar



Ahmed Nooruddin Mulla



Priyanshu Bhargav

Date: Dec 15, 2023

Features





Bluetooth Control: Navigate and control cleaning modes using a smartphone or computer.



Dual Functionality: Vacuuming for dust/debris and mopping for wet cleaning.



Cost-Effective Design: Built with accessible components for affordability.



Portable: Powered by a 9V battery for easy mobility.



Customizable: Open-source code allows modifications for specific needs.

Hardware Requirements





Arduino UNO



Bluetooth Module (HC-05)



12V DC Motors (x2) for navigation



Arduino Motor Driver (L298N)



9V Battery



1.5V Motor for mopping



Chassis and Wheels



Vacuum Module



Mop Attachment

Software Requirements





Arduino IDE: For uploading code to the Arduino UNO.



Bluetooth Terminal App: For sending commands (e.g., Bluetooth Serial Controller for Android).



Operating System: Windows, macOS, or Linux for development.

Installation





Clone the Repository:

git clone https://github.com/username/floor-cleaning-robot.git



Set Up Hardware:





Assemble the chassis and mount the DC motors to the wheels.



Connect the motors to the L298N motor driver.



Interface the Arduino UNO with the motor driver and HC-05 Bluetooth module.



Attach the vacuum module and 1.5V mop motor.



Power the system with a 9V battery.



Install Arduino IDE:





Download and install from arduino.cc.



Install the SoftwareSerial library if not already included.



Upload Code:





Open floor_cleaning_robot.ino in the Arduino IDE.



Connect the Arduino UNO to your computer via USB.



Upload the code to the Arduino.



Pair Bluetooth:





Power on the robot and pair the HC-05 module with your device (default password: 1234 or 0000).



Use a Bluetooth terminal app to send commands.

Usage





Power On: Turn on the robot and ensure the Bluetooth module is active.



Connect via App: Use a Bluetooth terminal app to connect to the HC-05 module.



Send Commands:





F: Move forward



B: Move backward



L: Turn left



R: Turn right



M: Activate mopping



V: Activate vacuum



S: Stop all operations



Cleaning: Navigate the robot to clean desired areas, toggling vacuum or mop as needed.



Power Off: Stop the robot and disconnect the battery when done.

Example Command Sequence:





Send F to move forward.



Send M to start mopping.



Send S to stop.

Code Structure





floor_cleaning_robot.ino: Main Arduino sketch for controlling the robot.





Handles Bluetooth communication.



Manages motor control for navigation and mopping.



Synchronizes vacuum operation.



Documentation:





docs/Floor_Cleaning_Robot_Report.md: Detailed project report.



docs/schematics/: Wiring diagrams (to be added).


Testing and Results





Navigation: Successfully moved in all directions via Bluetooth commands.



Cleaning: Vacuumed small debris and mopped light stains effectively.



Battery Life: Operated for 30-40 minutes on a 9V battery.



Challenges:





Occasional Bluetooth connectivity issues.



Limited battery life and vacuum capacity for larger debris.

Limitations and Future Improvements

Current Limitations:





Short battery life restricts continuous use.



Vacuum struggles with larger debris.



Bluetooth range limited to ~10 meters.

Planned Improvements:





Upgrade to a Li-ion battery for longer operation.



Add ultrasonic sensors for obstacle detection and autonomous navigation.



Enhance vacuum module for better debris handling.



Develop a custom mobile app for a seamless user experience.

Contributing

Contributions are welcome! To contribute:





Fork the repository.



Create a new branch (git checkout -b feature-branch).



Make your changes and commit (git commit -m "Add feature").



Push to the branch (git push origin feature-branch).



Open a Pull Request.

Please ensure your code follows the project's coding style and includes relevant tests.

License

This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments





Vidyashilp University for providing resources and support.



Faculty mentors for their guidance.



Open-source communities for Arduino and Bluetooth libraries.
