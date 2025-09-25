# Mobility Management

## General Vehicle Design

The robotic vehicle is constructed upon a **3D printed PETG chassis**. It's powered through the rear axle using a **3V–6V Dual Axis TT Gear Motor** and steered with a **Geekservo 2kg 360° servo**. It counts with two **HC-SR04 Ultrasonic Distance Sensors** to detect the track's walls in order to avoid collisions, a **HUSKYLENS Smart Vision Sensor** to detect incoming traffic signs and identify their color and a **TCS3200 Color Sensor Module**. All systems are controlled by an **Arduino UNO R4 WiFi** with a **Module L298P Motor Shield HW-723**.

## Chassis

We use a custom **3D printed PETG chassis** designed using Fusion 360. This vehicle frame is custom fitted with a space for our **two Slot 18650 Battery Holder**, an **Arduino UNO R4 WiFi** holder, a bracket for our **3V–6V Dual Axis TT Gear Motor**, a LEGO compatible 3x9 Technic axle hole plate to secure our steering, **Geekservo 2kg 360° servo** and the **HUSKYLENS Smart Vision Sensor's** mount, holes for our **HC-SR04 Ultrasonic Distance Sensors** and a mount for our **TCS3200 Color Sensor Module**. This simple design gives us ease of repair and modification, high ground clearance and torsional rigidity. It's an effective design which adapts to our robot's needs.

![ladder frame 450 px](https://github.com/user-attachments/assets/d033e1b5-6092-41a4-9a70-7b7c35e30245)

![ladder chassis drawing 450 px](https://github.com/user-attachments/assets/63a85143-5e66-408b-8fa5-6684a05fd3c3)

## Rear Axle

We power our drivetrain using a **Geekservo 2kg motor**, which is connected to our rear axle through a **custom LEGO gearbox** with a **1:3 gear ratio**, this means the follower gear rotates 3 times per each rotation of the driver gear, increasing speed 3 times and decreasing torque 3 times. Our rear axle is responsible for the forward and backward motion on our robot. This rear wheel drive design eliminates the necessity for constant velocity (CV) joints without sacrificing torque, speed and traction.

<img width="450" height="448" alt="geekservo motor 450 px" src="https://github.com/user-attachments/assets/3e6b2bc2-f8ef-4da9-a372-272d3d27e361" />


![gearbox 450 px](https://github.com/user-attachments/assets/6c10aa01-75c3-4df3-8871-256c79907bfb)

## Steering

We use an **Ackermann steering**, controlled by our **Geekservo 2kg 360° servo**. The Ackermann principle allows our vehicle's wheels to turn at different angles during a turn, ensuring they follow concentric circles with a common center point. We control the steering using degrees thanks to the **Geekservo 2kg 360° servo**, which makes it easier to program and improves the robot's accuracy.

![ackermann steering 450 px](https://github.com/user-attachments/assets/a6b9b996-2580-49a3-840b-4c39ff49bd6b)

