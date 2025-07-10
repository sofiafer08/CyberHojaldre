CyberHojaldre - Future Engineers
====

## Team Presentation

We are ***CyberHojaldre***, composed by Emilia Lever, Sofía Fernández, and Antonio Franco, a dedicated team representing the Thomas Jefferson School in the Future Engineers category of the WRO® 2025. Guided by our passion for robotics and inspired by the 2025 season theme “The Future of Robots” —which explores how autonomous systems can shape tomorrow’s world, from smart cities and sustainable infrastructure to space exploration— we have embarked on an ambitious journey to design, build, and program an autonomous four-wheeled robotic vehicle capable of navigating a randomized course on its own.


## Team Members

### Sofía Fernández

**Age:** 16 years old.

**Team role:** GitHub master, team spirit leader, and marketing director.

![fotito sofi con pop 450px](https://github.com/user-attachments/assets/c3ba33b2-c8ce-4c3d-9c67-56cd106d86f9)

### Emilia Lever
**Age:** 15 years old.

**Team role:** Silly, geeky programmer.

![Fotito Emilia 450px](https://github.com/user-attachments/assets/867450cc-e837-4dd9-a26e-c205a49c0907)

### Antonio Franco
**Age:** 14 years old.

**Team role:** Goofy designer and mechanics lead, invested in every part of the project.

![Foto de toño working 450px](https://github.com/user-attachments/assets/905fb398-edc0-4923-b230-d9369edf9215)


## Contents

* `t-photos` contains 2 photos of the team (an official one and one funny photo with all team members)
* `v-photos` contains 6 photos of the vehicle (from every side, from top and bottom)
* `video` contains the video.md file with the link to a video where driving demonstration exists
* `schemes` contains one or several schematic diagrams in form of JPEG, PNG or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `src` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.


## Robot Objectives

Our robot, ***POP***, is designed to autonomously complete the driving challenge by detecting and avoiding obstacles in the track's controlled environment. The robot monitors the track boundaries to ensure it stays within limits and maintains accurate navigation. It also can visually detect obstacles, allowing the robot to respond intelligently in real time by adjusting its path to avoid collisions depending on the obstacle's color. Beyond technical goals, one of our team's most important objectives is to enjoy the process, learn through experimentation and have fun building a robot that reflects both our creativity and our passion for robotics.


## Mobility Management

### General vehicle design

The robotic vehicle is constructed upon a **ladder chassis**. It's powered through the rear axle using a **Geekservo 2kg motor** and steered with a **Geekservo 2kg 360° servo**. It counts with three **HC-SR04 Ultrasonic Distance Sensors** and it's controlled by a **Micro:bit V2** with a **Wukong Breakout Board**.

### Chassis

We use a custom LEGO compatible PLA 3D printed **ladder chassis**. This vehicle frame is characterized by having two parallel longitudinal rails (like the sides of a ladder) connected by cross members. This simple design gives us ease of repair and modification, high ground clearance and torsional rigidity. It's an effective design which adapts to our robot's needs.

### Rear axle and power.

We power our drivetrain using a **Geekservo 2kg motor**, which is directly connected to our rear axle and responsible for the forward and backward motion on our robot. This rear wheel drive design eliminates the necessity for constant velocity (CV) joints without sacrificing torque, speed and traction.

### Steering.

We use an **Ackermann steering**, controlled by our **Geekservo 2kg 360° servo**. The Ackermann principle allows our vehicle's wheels to turn at different angles during a turn, ensuring they follow concentric circles with a common center point. We control the steering using degrees thanks to the **Geekservo 2kg 360° servo**, which makes it easier to program and improves the robot's accuracy.


## Power and Sensor Management

### Power Source

The power source of ***POP*** is a Li-ion battery pack with a nominal voltage of 3.7 V DC and a storage capacity of 400mAh.

### Sensors

We used three HC-SR04 Ultrasonic Distance Sensors. Each sensor provides 2cm to 400cm of non-contact measurement functionality with a ranging accuracy that can reach up to 3mm. Each HC-SR04 module includes an ultrasonic transmitter, a receiver and a control circuit. We placed a sensor on each side (left and right) and one in the front. The purpose is to provide the vehicle with the information needed to complete the challenges.


## Open Challenge Programming

Our open challenge programming works by establishing a variable for the two values of the lateral ultrasonic sensors and then creating a time variable that ends once the robot has completed its course. Our robot completes the course in an approximate time of **90s**, this means that once the time passes, the rear axle's motor value is set to zero and our robot stops. A conditional is added in which if the distance of both ultrasonic sensors is greater than **45cm**, then the front steering goes straight. Then, if the distance between the left sensor is less than **50cm** and greater than zero, the servo in our steering will move right by being set on **210°** and pause for **200ms**. The same happens with the right ultrasonic sensor, if the distance between the right sensor is less than **50cm**, then the servo will move to **150°**, this will cause it to move left, and then pause for **200ms** the same way it happened with the left sensor.


## Programming Challenge Obstacles

Although for this regional we weren't able to complete the programming for the obstacle course, we plan to incorporate it further along. We will use a HuskyLens camera that is capable of identifying colors and objects and storing the information in its database. The stored data will be implemented into the programming so as to steer clear of obstacles by indicating the color of the object, and then moving either left or right accordingly.


## Components 

### List of components:

| Quantity | Name | Image | 
|----------|------|-------|
| 1 | **Wukong Breakout Board (EF08207):** Wukong Breakout Board is a dual motor driving shield for Micro:bit. It extends our robot's capacity, allowing it to connect various sensors and electric modules. |![Wukong 356](https://github.com/user-attachments/assets/f61d7b43-7f9b-4200-968f-b53a5e719830)|
| 1 | **Micro:bit V2:** Micro:bit V2 is an open source hardware ARM-based embedded system, containing a Cortex-M4F microcontroller. It controls all of our robot's functions, from our drivetrain to our Huskylens camera. | ![micro bit foto fr ](https://github.com/user-attachments/assets/63ed836f-7a6b-4cb8-be16-7a6c6e5b936f)|
| 3 | **Ultrasonic Sensor HC-SR04:** This ultrasonic sensor provides 2cm to 400cm of non-contact measurement functionality which allows our robot to detect the track's limits. | ![actual sensor hc foto](https://github.com/user-attachments/assets/c071d810-4a04-4574-bedc-33bf450cf54f)|
| 1 | **Geekservo 2kg 360° Servo:** This servomotor offers 360° dual output axles with LEGO compatibility, which we use for our ackerman steering system. |![geek servo foto ](https://github.com/user-attachments/assets/1e684391-a7db-41d3-aa21-46279865f448)|
| 1 | **Geekservo 2kg Motor:** This motor offers high power with dual output LEGO axles, which we use to provide power to our rear wheel drive.  | ![red motoro foto ](https://github.com/user-attachments/assets/4c64a7d7-cd24-4a07-8d68-9547b2d9988b)| 
| 1 | **3D printed LEGO compatible ladder chassis:** Custom designed chassis to place all of the electromechanical components. | ![Foto chasis 356](https://github.com/user-attachments/assets/bcf54100-cc62-41cf-b7a2-986d5c706e9e) |
| 1 | **3D printed LEGO compatible ultrasonic sensor support:** Custom designed 45° angled mount for our three ultrasonic sensors. | ![Base de ultrasonicos foto](https://github.com/user-attachments/assets/e4c0f42d-7b86-46fa-a101-3e69117f5fc4) |
