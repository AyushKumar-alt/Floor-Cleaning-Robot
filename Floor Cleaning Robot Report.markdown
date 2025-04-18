# Floor Cleaning Robot Project Report

**Vidyashilp University, Bangalore**\
**Design Workshop**\
**Team Members**: Ayush Kumar, Ahmed Nooruddin Mulla, Priyanshu Bhargav\
**Date**: Dec 15, 2023

## Table of Contents

1. Abstract
2. Introduction
3. Objectives
4. System Design
   - 4.1 Components Used
   - 4.2 System Architecture
   - 4.3 Workflow
5. Implementation
   - 5.1 Hardware Assembly
   - 5.2 Software Development
   - 5.3 Testing
6. Results and Discussion
7. Conclusion
8. References
9. Acknowledgments

## Abstract

This report details the design and development of a Floor Cleaning Robot prototype aimed at enhancing the efficiency and convenience of domestic cleaning. The prototype integrates a vacuum and mopping system, controlled via Bluetooth, to cater to modern household needs. By leveraging affordable components like the Arduino UNO and DC motors, the project contributes to the growing market of domestic robotics, offering a cost-effective and user-friendly cleaning solution.

## 1. Introduction

The Floor Cleaning Robot prototype addresses the increasing demand for automated cleaning solutions in homes. With domestic robots becoming integral to daily life, this project focuses on creating an innovative, efficient, and adaptable cleaning device. The robot is designed to vacuum and mop floors, reducing manual effort while ensuring a thorough cleaning experience. Key objectives include ease of use, affordability, and adaptability to various floor types and user preferences.

## 2. Objectives

- Develop a functional prototype of a floor cleaning robot.
- Implement Bluetooth-based remote control for user convenience.
- Ensure cost-effectiveness using accessible components.
- Provide dual functionality: vacuuming and mopping.
- Contribute to the domestic robotics market with an innovative solution.

## 3. System Design

### 3.1 Components Used

The robot is built with the following components:

- **Arduino UNO**: Serves as the microcontroller to manage inputs and outputs.
- **Bluetooth Module (HC-05)**: Enables wireless communication for remote control.
- **12V DC Motors (x2)**: Drive the robot's wheels for movement.
- **Arduino Motor Driver (L298N)**: Controls the speed and direction of the DC motors.
- **9V Battery**: Powers the Arduino and Bluetooth module.
- **1.5V Motor**: Operates the mopping mechanism.
- **Chassis and Wheels**: Provide structural support and mobility.
- **Vacuum Module**: Handles debris collection.
- **Mop Attachment**: Facilitates wet cleaning.

### 3.2 System Architecture

The robot operates as a cohesive system:

- The Arduino UNO processes commands received via the Bluetooth module from a smartphone or computer.
- The motor driver translates these commands to control the 12V DC motors for navigation.
- A separate 1.5V motor activates the mopping mechanism.
- The vacuum module runs concurrently to collect dust and debris.
- Power is supplied by a 9V battery, ensuring portability.

### 3.3 Workflow

1. **Initialization**: The robot powers on, and the Bluetooth module pairs with a control device.
2. **Command Input**: Users send directional commands (forward, backward, left, right) or activate mopping/vacuuming via a mobile app.
3. **Navigation**: The Arduino processes commands, and the motor driver adjusts wheel movement.
4. **Cleaning**: The vacuum and mop operate based on user input or pre-programmed modes.
5. **Shutdown**: The robot stops when commanded or when the battery is depleted.

## 4. Implementation

### 4.1 Hardware Assembly

- The chassis was designed to house all components securely.
- DC motors were mounted to wheels, connected to the motor driver.
- The Arduino UNO was interfaced with the motor driver and Bluetooth module.
- The vacuum module and mop motor were integrated into the chassis.
- A 9V battery was connected to power the system.

### 4.2 Software Development

The control software was developed using the Arduino IDE. The code handles:

- Bluetooth communication for receiving user commands.
- Motor control for navigation and mopping.
- Vacuum operation synchronization.

**Sample Arduino Code** (simplified for brevity):

```cpp
#include <SoftwareSerial.h>
SoftwareSerial bluetooth(10, 11); // RX, TX
int motorPin1 = 3, motorPin2 = 4, motorPin3 = 5, motorPin4 = 6;
int mopMotor = 9;

void setup() {
  bluetooth.begin(9600);
  pinMode(motorPin1, OUTPUT);
  pinMode(motorPin2, OUTPUT);
  pinMode(motorPin3, OUTPUT);
  pinMode(motorPin4, OUTPUT);
  pinMode(mopMotor, OUTPUT);
}

void loop() {
  if (bluetooth.available()) {
    char command = bluetooth.read();
    if (command == 'F') { // Forward
      digitalWrite(motorPin1, HIGH);
      digitalWrite(motorPin2, LOW);
      digitalWrite(motorPin3, HIGH);
      digitalWrite(motorPin4, LOW);
    } else if (command == 'M') { // Mop
      digitalWrite(mopMotor, HIGH);
    } else if (command == 'S') { // Stop
      digitalWrite(motorPin1, LOW);
      digitalWrite(motorPin2, LOW);
      digitalWrite(motorPin3, LOW);
      digitalWrite(motorPin4, LOW);
      digitalWrite(mopMotor, LOW);
    }
  }
}
```

**Code Link**: GitHub Repository (Note: Original document's code link was incomplete; a placeholder is used here.)

### 4.3 Testing

- **Navigation Test**: The robot successfully moved in all directions based on Bluetooth commands.
- **Cleaning Test**: The vacuum collected small debris, and the mop cleaned light stains.
- **Battery Life**: The 9V battery supported 30-40 minutes of operation.
- **Challenges**: Occasional Bluetooth connectivity issues and limited battery life were noted.

## 5. Results and Discussion

The prototype successfully demonstrated:

- Reliable navigation via Bluetooth control.
- Effective vacuuming and mopping on smooth surfaces.
- Cost-effective design using affordable components.

**Limitations**:

- Short battery life limits continuous operation.
- The vacuum struggles with larger debris.
- Bluetooth range is limited to 10 meters.

**Future Improvements**:

- Upgrade to a higher-capacity battery (e.g., Li-ion).
- Incorporate sensors for obstacle detection and autonomous navigation.
- Enhance the vacuum module for better debris handling.
- Develop a dedicated mobile app for improved user interface.

## 6. Conclusion

The Floor Cleaning Robot prototype is a promising step toward accessible and efficient domestic cleaning solutions. By integrating vacuuming and mopping functionalities with Bluetooth control, the robot meets basic user needs while remaining cost-effective. Future iterations with advanced sensors and improved power management could position it as a competitive product in the domestic robotics market.

## 7. References

- Arduino Official Documentation: https://www.arduino.cc/
- Bluetooth HC-05 Module Guide: \[External Resource\]
- L298N Motor Driver Specifications: \[External Resource\]

## 8. Acknowledgments

We thank Vidyashilp University for providing the resources and guidance for this project. Special thanks to our faculty mentors and peers for their support.