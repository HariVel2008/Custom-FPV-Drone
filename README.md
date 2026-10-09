# Custom-FPV-Drone
Making a custom FPV Drone.
1. The Frame - FreeCAD design
2. The motors - undecided
3. The Props - undecided
4. The Flight Controller - Designed on KiCAD
5. The Electronic Speed Controller - Undecided
6. The Goggles - Undecided
8. The Receiver - Designed on KiCAD based on ExpressLRS (ELRS)
9. FPV Camera - Analog: Undecided

## Analog & Circuit Simulation Tools:
1. NgSPICE (embedded into KiCAD) - generates precise graphs using manufacturer data to model the circuit behavior.
2. ReNode - Open source simulation software that can simulate the STM32. Can also simulate external sensors and communication protocols such as I2C or SPI.
3. KiCAD built in ERC (Electrical Rules Checker) and DRC (Design Rules Checker)

## FPV Drone Parts Explained - https://www.youtube.com/watch?v=ndUVyEo2URM
1. Controller (Transmitter or Radio) - send a signal to the drone which is received by the receiver. Signal has an antenna. 
2. Flight Controller - the receiver sends the information to the flight controller.
3. Usually under the flight controller is the ESC (Electronic Speed Controller). Each motor gets its own ESC which is built into 1 board.
4. Camera captures a video which transfers the information down to the flight controller. Flight controller has an on screen chip which will interpret and signal goes to the video transmitter to transmit the video.
5. The power source for drones are usually LiPo batteries. Lithium Polymer batteries. Battiers are most likely connected with (big)XT60 or (small)XT30 for discharging or BT2.0 (smallest). You got to use a balance charge to charge the LiPo Battery.

## FPV Component Compatability
1. Radio protocol - ExpressLRS (ELRS).
2. Frequency - 2.4 gigahertz
3. Receiver also has to be ELRS and 2.4 gigahertz
4. Analog and digital are the two types of protocols. We are going to use analog with 5.8 gigahertz

## UARTS - a spot to connect an electrical component
1. each connection will have an R and T for each UART. It will also be connected to power and ground

## ESC Design Specifications
1. We need sensors such as IMU, magnetometer, barometer
2. We need a lot of IOs with various expansion capabilites
4. We will need a way to attach Raspberry Pi to the board later on for computer vision capabilites

<img width="540" height="345" alt="image" src="https://github.com/user-attachments/assets/081d1f62-ca97-4a6d-908d-78f6bc6de6d9" />

