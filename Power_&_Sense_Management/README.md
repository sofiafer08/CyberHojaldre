Power and Sensor Management
===

## Power Source

The power source of ***Captain ÑomÑom*** are **two 18650 Rechargeable Lithium-Ion Batteries**, each with a nominal voltage of **3.7 V DC** and a storage capacity of **2800 mAh**. They are coupled on a **two Slot 18650 Battery Holder** which is connected to the VMS (power input) and GND (negative ground connection) ports on our **Module L298P Motor Shield HW-723**. The shield regulates the voltage to 5V DC before supplying power to our **Arduino Uno R4**. Then, through our shield's 5V ports, we supply both of our **HC-SR04 Ultrasonic Distance Sensors**, our **HUSKYLENS Smart Vision Sensor**, our **TCS3200 Color Sensor Module**, our **SG90 9G Micro Servo** and our **3V–6V Dual Axis TT Gear Motor**.

![rechargeable-li-ion-battery 200](https://github.com/user-attachments/assets/abf8f06b-ad78-4fbc-835e-d01e77e46077)

## Sensors

### Ultrasonic Sensors

We used two **HC-SR04 Ultrasonic Distance Sensors**. Each sensor provides **2cm to 400cm** of non-contact measurement functionality with a ranging accuracy that can reach up to **3mm**. Each HC-SR04 module includes an ultrasonic transmitter, a receiver and a control circuit. We placed a sensor on each side (left and right) of our autonomous vehicle. Their purpose is to detect the track's walls in order to avoid collisions.

![rechargeable-li-ion-battery 200](https://github.com/user-attachments/assets/af8bfcec-93c7-4e1b-8576-6092b211318f)


### Color Sensor

We used a **TCS3200 Color Sensor Module**. The sensor can detect a wide variety of colors based on their wavelength. This sensor is specially useful for color recognition projects such as color matching and color sorting. Each TCS3200 module includes an array of photodiodes, filters for different colors, and a control circuit. Its purpose is to detect the diagonal lines which merge on the track's walls in order to make precise turns.

![color sensor 200](https://github.com/user-attachments/assets/2ab3d839-41a9-42f2-8112-a007d9c1f435)

### HuskyLens Camera

We used a **HUSKYLENS Smart Vision Sensor**. This sensor can detect and recognize objects, faces and colors using built-in AI algorithms. It is especially useful for projects involving computer vision, such as object tracking and autonomous navigation. Each HUSKYLENS module includes a camera, a processor for AI functions and a interface with a digital display and buttons. Its purpose is to detect incoming 

![Husky lens 200](https://github.com/user-attachments/assets/fb5a7aea-b139-4649-8c0e-841a44ab04ed)
