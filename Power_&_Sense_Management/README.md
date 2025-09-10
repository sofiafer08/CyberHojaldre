Power and Sensor Management
===

## Power Source

The power source of ***Captain ÑomÑom*** are **two 18650 Rechargeable Lithium-Ion Batteries**, each with a nominal voltage of **3.7 V DC** and a storage capacity of **2800 mAh**. They are coupled on a **two Slot 18650 Battery Holder** which is connected to the VMS (power input) and GND (negative ground connection) ports on our **Module L298P Motor Shield HW-723**. The shield regulates the voltage to 5V DC before supplying power to our **Arduino Uno R4**. Then, through our shield's 5V ports, we supply both of our **HC-SR04 Ultrasonic Distance Sensors**, our **HUSKYLENS Smart Vision Sensor**, our **TCS3200 Color Sensor Module**, our **SG90 9G Micro Servo** and our **3V–6V Dual Axis TT Gear Motor**.

![3 7 v battery 450 px](https://github.com/user-attachments/assets/0e918ebd-4e33-46e6-9e13-69211f99e40b)

## Sensors

We used two **HC-SR04 Ultrasonic Distance Sensors**. Each sensor provides **2cm to 400cm** of non-contact measurement functionality with a ranging accuracy that can reach up to **3mm**. Each HC-SR04 module includes an ultrasonic transmitter, a receiver and a control circuit. We placed a sensor on each side (left and right) of our autonomous vehicle. Their purpose is to detect 
