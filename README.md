Future Engineers
====

We are CyberHojaldre, composed by Emilia Lever, Sofia Fernandez, and Antonio Franco, a dedicated team representing the Thomas Jefferson School in the Future Engineers category of the WRO® 2025. Guided by our passion for robotics and inspired by the 2025 season theme “The Future of Robots”—which explores how autonomous systems can shape tomorrow’s world, from smart cities and sustainable infrastructure to space exploration—we have embarked on an ambitious journey to design, build, and program an autonomous four-wheeled robotic vehicle capable of navigating a randomized course on its own.

## Content

* `t-photos` contains 2 photos of the team (an official one and one funny photo with all team members)
* `v-photos` contains 6 photos of the vehicle (from every side, from top and bottom)
* `video` contains the video.md file with the link to a video where driving demonstration exists
* `schemes` contains one or several schematic diagrams in form of JPEG, PNG or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `src` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.


## Robot Objectives

Thw aim of Pop is to swiftly maneuver its environment. This involves: 

**Objectives**
1. Detect obstacles in the environment.
2. Avoid obstacles in the environment.
3. Complete three lapses 
4+. Have fun
+

## Mobility Management

Our robot, "POP", short for People is nice, works with the help of two motors. For the movement of the rear-axle we implemented a red "GeekServo" direct current (DC) motor, we chose it since it has a strong online community that already implements this motor using micro:bit software and hardware. It also has LEGO compatability, making it easier to adapt to our design. Our robot POP has a gray "GeekServo" servo motor as well. This controls the front-axle and provides the high-precision that is needed. This motor allows us to program it using degrees, which fits our team's need for accuracy.

The design of our chassis was made from scratch using Autodesk Fusion 360. Since the motors we agreed upon were compatible with LEGO components, it was only natural that our design was based on these same pieces. We have a simple structure inspired on a ladder-frame chassis, since our main objectives can be accomplished with a reliable base.



## Power and Sensor Management

**Power Source**

The power source of Pop is a Rechargeable Li-ion battery 2200 mAh type 18650 with a nominal voltage of 3.7 V DC and a storage capacity of 2,200 mAh. Made with a metal casing for greater safety and a lithium-ion active element.
We used three Ultrasonic Distance Sensors HC-SR04. This economical sensor provides 2cm to 400cm of non-contact measurement functionality with a ranging accuracy that can reach up to 3mm. Each HC-SR04 module includes an ultrasonic transmitter, a receiver and a control circuit. We place a sensor in each side (left and right) and one in the front. Its purpose is to provide the vehicle with the information needed to complete the challenges.


## Open Challenge Programming


Our open challenge programming works by establishing the two values of the ultrasonic sensors, and then creating a time variable that ends once the robot has completed its course. A conditional is added in which if the distance of both ultrasonic sensors is greater than x distance, then the front steering wheels goes straight. Then if the distance between the left sensor is less than x distance, then it will go right, and the same happens with the right ultrasonic sensors. If the distance between the right sensor is less that x distance, then it will go left.


## Programming Challenge Obstacles
## Components 

POP has a variety of parts that make up both his hardware and software. This includes: 

| Quantity | Name | Image | 
|----------|------|-------|
| 1 | **ELECFREAKS Micro:bit Motor:bit** : Motor:bit is a motor driving shield for Micro:bit which integrates a TB6612 motor driving chip. It extends our robot's capacity, allowing it to connect various sensors and electric modules. | ![motor bit foto](https://github.com/user-attachments/assets/73b395f8-b8a7-4a2f-8406-f71f2b36c786)|
| 1 | **Micro:bit V2** : Micro:bit V2 is an open source hardware ARM-based embedded system, containing a Cortex-M4F microcontroller. It controls all of our robot's functions, from our drivetrain to our Huskylens camera. | ![micro bit foto fr ](https://github.com/user-attachments/assets/63ed836f-7a6b-4cb8-be16-7a6c6e5b936f)|
| 3 | **Ultrasonic Sensor HC-SR04** : This ultrasonic sensor provides 2cm to 400cm of non-contact measurement functionality which allows our robot to detect the track's limits. | ![actual sensor hc foto](https://github.com/user-attachments/assets/c071d810-4a04-4574-bedc-33bf450cf54f)|
| 1 | **Geekservo 2kg 360° Servo** : This servomotor offers 360° dual output axles with LEGO compatibility, which we use for our ackerman steering system. |![geek servo foto ](https://github.com/user-attachments/assets/1e684391-a7db-41d3-aa21-46279865f448)|
| 1 | **Geekservo 2kg Motor** : This motor offers high power with dual output LEGO axles, which we use to provide power to our rear wheel drive.  | ![red motoro foto ](https://github.com/user-attachments/assets/4c64a7d7-cd24-4a07-8d68-9547b2d9988b)| 
| 1 | **3D printed chassis** | lol |








