Power and Sensor Management
===

## Power Source

### Batteries

The power source of ***Captain ÑomÑom*** are **two 18650 Rechargeable Lithium-Ion Batteries**, each with a nominal voltage of **3.7Vdc** and a storage capacity of **2800 mAh**. They are coupled on a **two Slot 18650 Battery Holder** which is connected to the VMS (power input) and GND (negative ground connection) ports on our **Module L298P Motor Shield HW-723**. The shield regulates the voltage to 5Vdc before supplying power to our **Arduino UNO R4 WiFi**. Then, through our shield's 5V ports, we supply both of our **HC-SR04 Ultrasonic Distance Sensors**, our **HUSKYLENS Smart Vision Sensor**, our **TCS3200 Color Sensor Module**, our **SG90 9G Micro Servo** and our **3Vdc ~ 6Vdc Dual Axis TT Gear Motor**.

![rechargeable-li-ion-battery 200](https://github.com/user-attachments/assets/abf8f06b-ad78-4fbc-835e-d01e77e46077)

**Key Specifications:**
* **Nominal Voltage:** 3.6 Vdc ~ 3.7 Vdc
* **Nominal Capacity:** 2800 mAh
* **Cycle Life:** ~500 cycles (to 80% capacity)

For more information, [*click here*](https://www.tinytronics.nl/product_files/004721_TENPOWER_INR18650-28HE_datasheet.pdf) to open the 18650 Rechargeable Lithium-Ion Battery's datasheet.

## Sensors

### Ultrasonic Sensors

We used two **HC-SR04 Ultrasonic Distance Sensors**. Each sensor provides **2cm to 400cm** of non-contact measurement functionality with a ranging accuracy that can reach up to **3mm**. Each HC-SR04 module includes an ultrasonic transmitter, a receiver and a control circuit. We placed a sensor on each side (left and right) of our autonomous vehicle. Their purpose is to detect the track's walls in order to avoid collisions.

![ultrasonic sensor 200](https://github.com/user-attachments/assets/6632f6f2-d8f8-4e4d-a60d-f3a8f5e15b7c)

**Key Specifications:**
* **Operating Voltage:** 3.3Vdc ~ 5Vdc
* **Quiescent Current:** <2mA
* **Operating Current:** 15mA
* **Operating Frequency:** 40KHz
* **Operating Range & Accuracy:** 2cm ~ 400cm ( 1in ~ 13ft) ± 3mm
* **Sensitivity:** -65dB min
* **Sound Pressure:** 112dB
* **Effective Angle:** 15°
* **Connector:** 4-pins header with 2.54mm pitch
* **Dimension:** 45mm x 20mm x 15mm
* **Weight:** 9g

For more information, [*click here*](https://www.handsontec.com/dataspecs/HC-SR04-Ultrasonic.pdf) to open the HC-SR04 Ultrasonic Distance Sensor's datasheet.

### Color Sensor

We used a **TCS3200 Color Sensor Module**. The sensor can detect a wide variety of colors based on their wavelength. This sensor is specially useful for color recognition projects such as color matching and color sorting. Each TCS3200 module includes an array of photodiodes, filters for different colors, and a control circuit. Its purpose is to detect the diagonal lines which merge on the track's walls in order to make precise turns.

![color sensor 200](https://github.com/user-attachments/assets/2ab3d839-41a9-42f2-8112-a007d9c1f435)

**Key Specifications:**
* **Operating Voltage:** 2.7Vdc ~ 5.5Vdc
* **Photodiodes:** 64 total (16 red, 16 green, 16 blue, 16 clear)
* **Operating Range & Accuracy:** Best at 1–3 cm from the object
* **Extras on module:** Includes 4 white LEDs for consistent illumination

For more information, [*click here*](https://www.mouser.com/catalog/specsheets/tcs3200-e11.pdf?srsltid=AfmBOorEgZGDruwtI3xHOg00w5BmGMS5fNyywV3p9RMySATtGV3V-sCV) to open the TCS3200 Color Sensor Module's datasheet.

### HuskyLens Camera

We used a **HUSKYLENS Smart Vision Sensor**. This sensor can detect and recognize objects, faces and colors using built-in AI algorithms. It is especially useful for projects involving computer vision, such as object tracking and autonomous navigation. Each HUSKYLENS module includes a camera, a processor for AI functions and a interface with a digital display and buttons. Its purpose is to detect incoming trafic signs and identify their color in order to indicate our vehicle side of the lane it must follow in the obstacle challenge.

![Husky lens 200](https://github.com/user-attachments/assets/fb5a7aea-b139-4649-8c0e-841a44ab04ed)

**Key Specifications:**
* **Processor:** Kendryte K210
* **Image Sensor:** OV2640 (2.0 Megapixel Camera)
* **Operating Voltage:** 3.3Vdc ~ 5Vdc
* **Current Consumption (TYP):** 320mA 3.3Vdc, 230mA 5Vdc (face recognition mode; 80% backlight brightness; fill light off)
* **Connection Interface:** UART, I2C
* **Display:** 2in IPS screen with 320 x 240 resolution
* **Built-in Algorithms:** Face Recognition, Object Tracking, Object Recognition, Line Tracking, Color Recognition, Tag Recognition
* **Dimension:** 52mm x 44.5mm

For more information, [*click here*](https://www.farnell.com/datasheets/3178377.pdf) to open the HUSKYLENS Smart Vision Sensor.
