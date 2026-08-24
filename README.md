# Tello Drone Controller

Java application for controlling a DJI Tello drone over Wi-Fi using an object-oriented architecture that separates device state, movement commands and network communication.

## Overview

This project explores direct communication with physical hardware through the Tello command interface. Instead of concentrating all behavior in a single class, the implementation separates the drone model, movement operations, controller logic and network communication into dedicated components.

It is a compact project, but it demonstrates a different engineering context from my web applications: Java, object-oriented design, UDP-style device communication and command-driven interaction with hardware.

## Features

- Connect to a DJI Tello over its Wi-Fi network
- Send flight and movement commands
- Trigger takeoff, landing and rotations
- Read and expose drone status information
- Interactive terminal-based control flow
- Modular object-oriented design

## Architecture

```text
Terminal / Main
      |
      v
DroneController
   /       \
  v         v
Drone     DroneMovement
  |           |
  +-----------+
      |
      v
ComandoRede
      |
      v
DJI Tello
```

## Main components

- `Main.java`: application entry point and command flow
- `Drone.java`: drone state and core representation
- `DroneController.java`: coordinates user actions and drone operations
- `DroneMovement.java`: movement-related behavior
- `DroneMoves.java`: supported movement definitions
- `DroneStatus.java`: drone status representation
- `ComandoRede.java`: network communication with the device

## Stack

- Java
- Maven
- Object-oriented programming
- Network communication
- DJI Tello command interface

## Requirements

- Java 11 or newer
- Maven-compatible environment
- Computer connected to the DJI Tello Wi-Fi network

## Running

```bash
mvn compile
mvn exec:java
```

The exact execution command may vary depending on the local Maven configuration. The machine running the application must be connected to the drone network.

## What this project demonstrates

- Object-oriented modeling
- Separation of responsibilities
- Hardware communication from Java
- Command abstraction
- Device state management
- Working outside a browser/server application stack

## Status

Learning and portfolio project focused on Java and hardware integration.
