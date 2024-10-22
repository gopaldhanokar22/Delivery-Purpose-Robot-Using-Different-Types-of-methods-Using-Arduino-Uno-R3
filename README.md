# Delivery Purpose Robot Using Different Types of methods Using Arduino Uno R3

### Introduction :
The project is design to Delivery robot build a line following, obstacle avoidance, IR remote control, voice control, light following, human following, using some different type of sensors for its movement. Arduino uno and different ICs used to achieve the desired operation. A robot is a machine that can perform task automatically or with guidance. The project proposes robot that has an intelligence built in it such that it directs itself whenever an obstacle comes in its path. This robot is built, using Arduino. An ultrasonic sensor is used to detect any obstacle ahead of it and sends a command to the Arduino. Depending on the input signal received, the Arduino redirects the robot to move in an alternate direction by actuating the motors which are interfaced to it through a motor driver. At the same time, we can control steering gear to realize the obstacle avoidance function. That is one function on robot similar as different type of function also perform. The robot uses front axle steering, rear wheel drive arrangement. Four drive tires are driven by Four DC motors with gear reduction mechanisms.

### Block Diagram : 
1) Line Following

<img width="464" alt="Screenshot 2024-10-22 171814" src="https://github.com/user-attachments/assets/ea7d072b-e483-4d50-a85c-c69d302886a5">

2) Obstacle Avoiding

<img width="464" alt="Screenshot 2024-10-22 171914" src="https://github.com/user-attachments/assets/06b00c8f-0793-4e0c-838b-e9ff975b29a2">

3) Voice Control

<img width="452" alt="Screenshot 2024-10-22 171947" src="https://github.com/user-attachments/assets/5b4a3993-c21b-49fc-a466-52366eff7aeb">

4) Light Following

<img width="461" alt="Screenshot 2024-10-22 172022" src="https://github.com/user-attachments/assets/f23db037-492e-4691-adbd-ac071018859b">

5) Human Following

<img width="507" alt="Screenshot 2024-10-22 172104" src="https://github.com/user-attachments/assets/91c8a61a-deb5-4c5f-a7e1-67130007b1cf">

### Hardware : 
1. Arduino Uno R3 
2. L298 Motor Driver 
3. DC motor 
4. HC-05 Bluetooth Module 
5. Infrared IR Wireless 
6. Remote Control Module 
7. IR Sensor 
8. Ultrasonic Sensor Holder 
9. Servo Motor 
10. Ultrasonic Sensor hc-sr0 
11. Jumper Wires 
12. LED 
13. LM358 Dual Operational Amplifier 
14. 10k Variable Resistor 
15. BD139 NPN Transistor 
16. 4148 Diode 
17. LDR Sensor 
18. Resistor 
19. Capacitor 
20. TIP32C Transistor 
21. 18650 3.7V 1200mAh Lithium-Ion Rechargeable Cell 
22. On/Off switch

### Software :
1. Proteus 8TM software 
2. Arduino IDE 
3. Easy EDA

### Pin Connection 

1) Connect L298 Motor Driver to Arduino UNO:

<img width="581" alt="Screenshot 2024-10-22 172432" src="https://github.com/user-attachments/assets/23df4a86-5281-40e7-a421-d174e230a74e">

2) Connect L298 Motor Driver to DC motor: 

<img width="587" alt="Screenshot 2024-10-22 172508" src="https://github.com/user-attachments/assets/44aaedd4-47d1-4df8-a030-baf0bc66ac58">


Notes: We will connect the motors in criss cross pattern. This is because we have to make the car in such a way that two side motor rotates in same direction in order to go Forward Backward and other known directions

3) Connect IR Sensors for line following to Arduino UNO:

<img width="577" alt="Screenshot 2024-10-22 172619" src="https://github.com/user-attachments/assets/baf59706-42a9-4069-b08f-7167d169f223">

4) Connect IR Sensors for human following to Arduino UNO:

<img width="572" alt="Screenshot 2024-10-22 172709" src="https://github.com/user-attachments/assets/bfcd6144-b762-4ea5-8841-553dfea3462e">

5) Connect Ultrasonic sensor to Arduino UNO:

<img width="575" alt="Screenshot 2024-10-22 172749" src="https://github.com/user-attachments/assets/744d7378-2489-4764-8fc0-4756194da5af">

6) Connect Bluetooth Module to Arduino UNO:

<img width="573" alt="Screenshot 2024-10-22 172832" src="https://github.com/user-attachments/assets/8fc48598-63c2-41f4-af69-2ba9e195178a">

7) Connect Servo motor to Arduino UNO:

<img width="577" alt="Screenshot 2024-10-22 172904" src="https://github.com/user-attachments/assets/2e8fcd30-c06e-4cc3-8019-102069f5bcf6">

8) Connection of Light following robot

<img width="560" alt="Screenshot 2024-10-22 172945" src="https://github.com/user-attachments/assets/02a34734-2e1d-46f2-b8cd-c503f21f5096">

### Working : 

1) Line Following: \
The concept of the line follower robot is related to the transmitting and receiving of light. The white colour reflects all the light that falls on it whereas the black colour absorbs all the light. In this line follower robot, we have used IR transmitters and receivers (also known as photodiodes). When IR light falls on a white surface, it gets reflected back towards the IR receiver, generating some voltage changes that are analyzed by the Arduino. When IR light falls on a black surface, it gets absorbed by the black surface, and no rays are reflected back thus, the IR receiver doesn’t receive any rays. In this project, when the IR sensor senses a white surface, an Arduino gets HIGH as input, and when it senses a black line, an Arduino gets LOW as input. Based on these inputs, an Arduino Uno provides the proper output to control the line follower.

2) Obstacle Avoiding: \
The obstacle avoidance robot uses ultrasonic sensors for its movements. A arduino Uno R3 is used to achieve the desired operation. The motors are connected through the motor driver L298 motor driver. The ultrasonic sensor is attached in front of the robot. Whenever the robot is going on the desired path the ultrasonic sensor transmits the ultrasonic waves continuously from its sensor head. Whenever an obstacle comes ahead of it the ultrasonic waves are reflected from an object and that information is passed to the microcontroller. The microcontroller controls the motors left, right, back, front, based on ultrasonic signals. To control the speed of each motor pulse width modulation is used (PWM).

3) Voice Control: \
The block diagram of the simple voice controlled robotic vehicle is given it consists of the smartphone that recognizes the voice commands and are being wirelessly transferred to the Bluetooth module HC05. The module at that point changes over the order to content and the series of characters are sent to the Arduino for additional handling. The Arduino microcontroller decodes the string got and correspondingly performs further capacities. The signals are sent to the motor that hence powers and drives the motors connected to it. On the Transmitter area, commands are given to the Mobile Application through the mic. This portable handset is associated with the moving vehicle by means of Bluetooth module. The portable application utilized, is modified so that the voice orders given to the handset are received by the mic and these simple voice orders are changed over to advanced word successions (A to D transformation). These stored sequences are than transmitted to the robotic vehicle via Bluetooth transceiver module and are sent to the transceiver controller. Android application transceiver is used to decode the received signal with the Bluetooth module. The controller contrasts these signals and the put away program orders in it and convert them into voice strings. The voice strings are then used to run the servo engines for the ideal interval of time.  The microcontroller, sends directions, which when executed, helps in working of the engine driver. The yield of the Arduino goes to the engine driver IC and it controls the specific engine. A DC power supply is required to run the system. The DC power supply feeds the Microcontroller and the Bluetooth module.

4)  IR Remote Control: \
We use TSOP Sensor Module for receiving the IR signals which we give through pressing buttons of a remote. Our robot can move in forward, backward, right, and left directions according to the given signals. We have to press the buttons of the remote to move the Robot in a particular direction. We use four LEDs of different colors which will go on as the robot moves in different directions.  it works as a Bluetooth control robot. If the Robot will move forward the LED on pin 3 will glow, the same for the backward LED on pin 4 will glow, the LED on pin 5 will glow if the robot moves in the right, and the LED on pin 6 will glow if the robot moves in left. The Robot keeps moving until we press the stop button on the remote. All the LEDs reset to off. In this way, the Robot moves.

5) Light Following: \
The robot uses a special electronic circuit to control the speed of two motors through the use of two light sensors. The motors are connected to the robot's wheels, which allow it to drive around. Figure 3 shows a simplified diagram of this process (continue reading for a more detailed description of the circuit). If both light sensors detect the same amount of light, the wheels spin at the same speed, so the robot goes straight. If one light sensor detects more light than the other, one wheel will spin faster, which will make the robot turn. A simplified diagram of how the robot works. The robot's circuit detects bright light (for example, from a flashlight). The circuit then sends electrical signals to the robot's motors to turn them on. The motors drive the robot's wheels, which make the robot move and steer.

6) Human Following: \
when you come near to the robot starts to follow you. there are 4 wheels in the robot. and 4 motors attached to the chassis. now there are three sensors on the robot one is an ultrasonic sensor and two IR sensor which arranges like two sensors left and right to the ultrasonic sensor. and when you put your hand near to the ultrasonic sensor the robot will start forward. If you turn your hand to the left side the Arduino robot moves on the left side, and if you put your hand in the right the robot will move in the right direction. so, how the whole system works we will talk about this. when you put your hand in from of the ultrasonic sensor then the sensor detects you and sends this information to the Arduino. there is some distance prefix in the Arduino so if your hand is away from the sensor, it will not read that. and if your hand is near to the sensor, it will read it. Now Arduino knows that there is something in front of the sensor and Arduino send some instruction to the motor driver and motor driver trigger the motors. and the Arduino robot starts to move forward we need to run all motor forward. Now, what about the sensors. IR sensor works on infrared light which can also detect the object near to it. so there is two IR sensor one is at the left side of ultrasonic sensor and other is at the right side of the ultrasonic sensor. when anything comes near to the left sensor Arduino got the information that there is something is near to the left sensors and according to the code, the robot will turn to the left. and the same process for the right sensor.

![Delivery Purpose Robot 4](https://github.com/user-attachments/assets/cf497287-5ec7-47cf-9847-1ceb18fcb3ac)

![Delivery Purpose Robot 6](https://github.com/user-attachments/assets/c62e2da2-c82d-4aee-ae3e-7d72207ea744)


![Delivery Purpose Robot 7](https://github.com/user-attachments/assets/d271ce94-f9e2-4a3c-8606-ceed81d0100d)
