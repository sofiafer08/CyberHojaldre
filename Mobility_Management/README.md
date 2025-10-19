# Mobility Management

## General Vehicle Design

The robotic vehicle is constructed upon a **3D printed PETG chassis**. It's powered through the rear axle using a **3V–6V Dual Axis TT Gear Motor** and steered with a **Geekservo 2kg 360° servo**. It counts with two **HC-SR04 Ultrasonic Distance Sensors** to detect the track's walls in order to avoid collisions, a **HUSKYLENS Smart Vision Sensor** to detect incoming traffic signs and identify their color and a **TCS3200 Color Sensor Module** which serves as a backup for the camera. All systems are controlled by an **Arduino UNO R4 WiFi** with a **Module L298P Motor Shield HW-723**.

## Drivetrain

### Rear-Wheel Drive

We power our drivetrain using a **3V–6V Dual Axis TT Gear Motor**, which is directly connected to the vehicle's rear axle. Our rear axle is responsible for the forward and backward motion on our robot. This rear wheel drive design eliminates the necessity for complex systems such as constant velocity (CV) joints or external gearboxes without sacrificing torque, speed, and traction; resulting in a reliable and easy to repair robot.

<img width="1500" height="1500" alt="marcos de fotos (10)" src="https://github.com/user-attachments/assets/6946bf64-8063-4ebf-b4b7-296f1527e204" />

### Steering

We use an **Ackermann steering** built using LEGO parts. This steering system is proven to be one of the most efficient and reliable which is demonstrated by its years of use in the automotive industry. The Ackermann principle ensures that a vehicle's inner front wheel turns at a greater angle than the outer front wheel during a turn, allowing both wheels to trace concentric circles around a single virtual pivot point. We control the steering using degrees thanks to the **Geekservo 2kg 360° servo**, which makes it easier to program and improves the robot's accuracy. This steering system also provides a wide range of movement, making the vehicle highly maneuverable.

<img width="" height="256" alt="image" src="https://github.com/user-attachments/assets/221cc844-8f50-4b0f-b352-cae766c9928f" />

<img width="450" height="" alt="image" src="https://github.com/user-attachments/assets/9ecb0b7e-72fd-41a1-a149-a63a72c827d8" />

## 3D Printed Parts

### Chassis

We use a custom **3D printed PETG chassis** designed using Fusion 360. This vehicle frame is custom fitted with a space for our **two Slot 18650 Battery Holder**, an **Arduino UNO R4 WiFi** holder, a bracket for our **3V–6V Dual Axis TT Gear Motor**, a LEGO compatible 3x9 Technic axle hole plate to secure our steering's **Geekservo 2kg 360° servo** and the **HUSKYLENS Smart Vision Sensor's** mount, holes for our **HC-SR04 Ultrasonic Distance Sensors** and a mount for our **TCS3200 Color Sensor Module**. This simple design gives us ease of repair, high ground clearance and torsional rigidity. It's an effective design which adapts to our robot's needs.

For more information, [*click here*](https://github.com/sofiafer08/CyberHojaldre/blob/main/Models_%26_Components/Chassis.stl) to open the Chassis Interactive stl.

<img width="1500" height="1500" alt="marcos de fotos (5)" src="https://github.com/user-attachments/assets/cb1cc562-0a2e-4d51-9033-56b336168af8" />

### Rear Axle Adapters

In order to directly connect our **3V–6V Dual Axis TT Gear Motor** to the vehicle's rear axle, we designed two **3D printed PETG adapters**. From one side, the adapter is able to connect to the **3V–6V Dual Axis TT Gear Motor's** axle, while from the other its able to couple with a LEGO Technic axle, allowing us to use LEGO wheels and tires to provide traction.

For more information, [*click here*](https://github.com/sofiafer08/CyberHojaldre/blob/main/Models_%26_Components/tt_Motor_Axle.stl) to open the Motor Axle Interactive stl

<img width="1500" height="1500" alt="marcos de fotos (7)" src="https://github.com/user-attachments/assets/50e593e8-a18d-4568-8d09-ea383653f1ec" />

### Camera Mount

The **HUSKYLENS Smart Vision Sensor** is installed in a **3D printed PETG camera mount**. This mount allows us to have a greater height and position the camera at a 45° angle during the robot's testing in order to enhance the range and accuracy. We connect it to the chassis LEGO pins, as both 3D printed pieces have LEGO compatibility. This modular piece amplifies the number of uses our camera has, changing easily the robot's capacities.

For more information, [*click here*](https://github.com/sofiafer08/CyberHojaldre/blob/main/Models_%26_Components/HuskyLens_Mount.stl) to open the HuskyLens Mount Interactive stl.

<img width="1500" height="1500" alt="marcos de fotos (8)" src="https://github.com/user-attachments/assets/9dc46e08-f4a3-483f-9642-d6895871a857" />
