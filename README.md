# Line Following Robot Arduino Code

Welcome to the GitHub repository for the CSE204 course project: Line Following Robot. This project focuses on designing and implementing a robot capable of autonomously following a line using various sensors and control algorithms. The repository includes detailed documentation, code, and schematics to help you understand and replicate our project. We hope you find this project both educational and inspiring.

Check out the project in action and connect with us on LinkedIn:[LinkedIn post](https://shorturl.at/B4KjK)


Feel free to explore the repository and contribute!

## Table of Contents

- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Code Structure](#code-structure)



## Features

- Line following using infrared sensors.
- Obstacle detection and avoidance with an ultrasonic sensor.
- PID-based control for smooth line following.
- Modular code structure for easy customization.

## Hardware Requirements

- Arduino board
- Infrared sensors (5 in this case)
- Ultrasonic sensor (NewPing library)
- Motor driver for controlling the motors
- Motors and wheels
- Chassis and power supply

## Software Requirements

- Arduino IDE
- NewPing library

## Installation

1. Clone the repository to your local machine.
   ```bash
   git clone https://github.com/sargis02/LineFollowingRobotCSE204.git
2.  Open the Arduino IDE.
3.  Load the **204lineFollower.ino** sketch.
4.  Install the **NewPing library** if not already installed. ([NewPing Library Download Link](https://www.arduino.cc/reference/en/libraries/newping/)).
5.  Connect your Arduino board to the computer and upload the sketch.

## Configuration

### Motor Configuration

#### Motor Pins

The robot uses a motor driver to control two DC motors. Adjust the pin assignments based on your specific wiring configuration.

```cpp
// Motor Pin Configuration
#define ena 10   // PWM pin for controlling the speed of the left motor
#define inA 9    // Motor driver input A for the left motor
#define inB 8    // Motor driver input B for the left motor
#define inC 7    // Motor driver input C for the right motor
#define inD 6    // Motor driver input D for the right motor
#define enb 5    // PWM pin for controlling the speed of the right motor
```

### Motor Direction

The following conventions are used for motor direction control:

- `inA` and `inB` control the direction of the left motor.
- `inC` and `inD` control the direction of the right motor.

Adjust these values based on your motor driver and motor wiring.

### Sensor Configuration

### Infrared Sensors

The robot uses five infrared sensors for line following. Connect these sensors to the specified analog pins.

```cpp
// Infrared Sensor Pins
const int irPins[5] = {A0, A1, A2, A3, A4};

```

## Code Structure

1. `setup()`: Initializes the robot's components.
2. `loop()`: Continuously executes line following and obstacle detection logic.
3. `line_follow()`: Implements the PID-based line following algorithm.
4. `ustad_samne_plastic()`: Stops the motors and indicates obstacle detection. > this feature is commented. 
5. `readSensor()`: Reads values from infrared sensors and calculates the error.
6. `wheel()`: Controls the motor speed based on input values.




