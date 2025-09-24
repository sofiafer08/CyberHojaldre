## Open Challenge Programming

For our previous robot we programmed using MakeCode for microbit. It consisted of a simple code that would rotate the servo to 210 degrees if the left ultrasonic sensor percieved a distance less than 45cm. The same would happen with the right ultrasonic sensor, but in that case the servo will rotate to 150 degrees. In the case that both sensors read a distance greater than 30cm, the servo was set to 180 degrees and it would continue its straight path. Once the time variable ended, the DC motor would be stopped, and our robot would park in the position it started. 

Since we developed **Captain ÑomÑom**, We have now programmed a new code that includes other components that facilitate Cap.'s cruising. 
+ It starts by establishing where each component is connect on the HW-723 shield. We then attribute values to the constants; **Max sequences** (Dictates how many times the color sensor must complete the detection sequence), **Reset delay** (Is responsible for the time that must pass between each color sensor reading.), **Shutdown delay** (Is how much time the robot will wait to shut down once it reaches max sequences.), **Center psoition** (Refers to the angle in which the servo motor will go straight.), and **Motor Speed** (Simply states the speed at which the DC motor will run.)
+ We also establish what the max and min angles are **114 degrees** and **74 degrees** respectively. This ensures that Cap. won't perform sharp turns that limit his movenment.
+ The next part of the code consists on assignig the RGB values of the color blue and orange so that it can accurately detect them during the rounds. Due to the similarities that both of these values share, we decided to use a green transparent sheet that would help us focus specifically on the R ranges. In order to have a consistent detection we used a **Minimum** and **Maxium** to create ea range. 
+ The global variables help keep track of the actions the robot is performing. It also establishes objects such as myservo that works as a tool for assigning functions to the physical servo. Inside tehm we can also find shutdownSequenceStarted. This refers to what happens after the color sensor read a certain color 12 times.
+ Void SetUp hapens only once when the robot is turned on. This sets up every motor an sensor so that everything is in place in order to start the loop.
+ When the loop starts, it first ensures that the maximun amount of sequences hasn't been reached so that it can continue with the loop. It also explains what to do in case the motor is stopped.
+ For color detection, the code 
 
|---|

Our open challenge programming works by establishing a variable for the two values of the lateral ultrasonic sensors and then creating a time variable that ends once the robot has completed its course. These variables are set as "sensor derch." (Right sensor), and "sensor izq." (Left sensor), so as to facilate the understanding of our code. 

Our robot completes the course in an approximate time of **90s**, this means that once the time passes, the rear axle's motor value is set to zero and our robot stops.

A conditional is added in which if the distance of both ultrasonic sensors is greater than **45cm**, then the front steering goes straight and pauses for **200ms**. If the distance between the left sensor is less than **50cm** and greater than zero, the servo in our steering will move right by being set on **210°** and pause for **200ms**. The same happens with the right ultrasonic sensor. If the distance between the right sensor is less than **50cm**, then the servo will be set to **150°**, this will cause it to move to the left, and then pause for **200ms** the same way it happened with the left sensor.

This code allows our robot **POP** to achieve 30 points consistently, since its able to go aorund the track 3 times, then park succesfully without coming into contact with any of the inner or outer walls. This is true for every starting position. 

## Obstacle Challenge Programming

For the obstacle challenge we seek to achieve 7 points by leaving the parking area inside the two pink walls. The code for this task is fairly simple. Seeing as **POP** is small enough to take a sharp turn and leave the space without bumping into the walls, we have a shortned version of our code for the open challenge. 

We begin by establishng the values of the two ultrasonic sensor as their own variable, and then **POP** will detect wether he is on the left or right side of the outer wall. Once he determines this, the front steering will turn to the opposite side, and he can leave the parking spot successfully. This is true no matter the direction in which he goes (Clock-wise or counter clock-wise)

