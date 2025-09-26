# Mobility Management

## General Vehicle Design

The robotic vehicle is constructed upon a **3D printed PETG chassis**. It's powered through the rear axle using a **3V–6V Dual Axis TT Gear Motor** and steered with a **Geekservo 2kg 360° servo**. It counts with two **HC-SR04 Ultrasonic Distance Sensors** to detect the track's walls in order to avoid collisions, a **HUSKYLENS Smart Vision Sensor** to detect incoming traffic signs and identify their color and a **TCS3200 Color Sensor Module** which serves as a backup for the camera. All systems are controlled by an **Arduino UNO R4 WiFi** with a **Module L298P Motor Shield HW-723**.

## Drivetrain

### Rear-Wheel Drive

We power our drivetrain using a **3V–6V Dual Axis TT Gear Motor**, which is directly connected to the vehicle's rear axle. Our rear axle is responsible for the forward and backward motion on our robot. This rear wheel drive design eliminates the necessity for complex systems such as constant velocity (CV) joints or external gearboxes without sacrificing torque, speed, and traction; resulting in a reliable and easy to repair robot.

<img width="" height="253" alt="image" src="https://github.com/user-attachments/assets/0eee9e03-8bb6-4b8d-b94d-10552d5ad2b8" />


<img width="450" height="" alt="image" src="https://github.com/user-attachments/assets/13899b38-ac24-4481-843e-970dbb9b70c7" />

### Steering

We use an **Ackermann steering** built using LEGO parts. This steering system is proven to be one of the most efficient and reliable which is demonstrated by its years of use in the automotive industry. The Ackermann principle ensures that a vehicle's inner front wheel turns at a greater angle than the outer front wheel during a turn, allowing both wheels to trace concentric circles around a single virtual pivot point. We control the steering using degrees thanks to the **Geekservo 2kg 360° servo**, which makes it easier to program and improves the robot's accuracy. This steering system also provides a wide range of movement, making the vehicle highly maneuverable.

<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/2e101e4c-5995-465d-b030-fe04e6145801" />

![ackermann steering 450 px](https://github.com/user-attachments/assets/a6b9b996-2580-49a3-840b-4c39ff49bd6b)

## 3D Printed Parts

### Chassis

We use a custom **3D printed PETG chassis** designed using Fusion 360. This vehicle frame is custom fitted with a space for our **two Slot 18650 Battery Holder**, an **Arduino UNO R4 WiFi** holder, a bracket for our **3V–6V Dual Axis TT Gear Motor**, a LEGO compatible 3x9 Technic axle hole plate to secure our steering's **Geekservo 2kg 360° servo** and the **HUSKYLENS Smart Vision Sensor's** mount, holes for our **HC-SR04 Ultrasonic Distance Sensors** and a mount for our **TCS3200 Color Sensor Module**. This simple design gives us ease of repair, high ground clearance and torsional rigidity. It's an effective design which adapts to our robot's needs.

### Rear Axle Adapters

In order to directly connect our **3V–6V Dual Axis TT Gear Motor** to the vehicle's rear axle, we designed two **3D printed PETG adapters**. From one side, the adapter is able to connect to the **3V–6V Dual Axis TT Gear Motor's** axle, while from the other its able to couple with a LEGO Technic axle, allowing us to use LEGO wheels and tires to provide traction.

### Camera Mount

The **HUSKYLENS Smart Vision Sensor** is installed in a **3D printed PETG camera mount**. This mount allows us to change the camera's height and angle during the robot's testing in order to enhance the range and accuracy. We connect it to the chassis LEGO pins, as both 3D printed pieces have LEGO compatibility. This modular piece amplifies the number of setups and uses our camera has, making changes later on easier and less time consuming.
