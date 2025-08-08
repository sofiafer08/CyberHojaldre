## Open Challenge Programming

Our open challenge programming works by establishing a variable for the two values of the lateral ultrasonic sensors and then creating a time variable that ends once the robot has completed its course. These variables are set as "sensor derch." (Right sensor), and "sensor izq." (Left sensor), so as to facilate the understanding of our code. 

Our robot completes the course in an approximate time of **90s**, this means that once the time passes, the rear axle's motor value is set to zero and our robot stops.

A conditional is added in which if the distance of both ultrasonic sensors is greater than **45cm**, then the front steering goes straight and pauses for **200ms**. If the distance between the left sensor is less than **50cm** and greater than zero, the servo in our steering will move right by being set on **210°** and pause for **200ms**. The same happens with the right ultrasonic sensor. If the distance between the right sensor is less than **50cm**, then the servo will be set to **150°**, this will cause it to move to the left, and then pause for **200ms** the same way it happened with the left sensor.

This code allows our robot **POP** to achieve 30 points consistently, since its able to go aorund the track 3 times, then park succesfully without coming into contact with any of the inner or outer walls. This is true for every starting position. 

## Obstacle Challenge Programming

For the obstacle challenge we seek to achieve 7 points by leaving the parking area inside the two pink walls. The code for this task is fairly simple. Seeing as **POP** is small enough to take a sharp turn and leave the space without bumping into the walls, we have a shortned version of our code for the open challenge. 

We begin by establishng the values of the two ultrasonic sensor as their own variable, and then **POP** will detect wether he is on the left or right side of the outer wall. Once he determines this, the front steering will turn to the opposite side, and he can leave the parking spot successfully. This is true no matter the direction in which he goes (Clock-wise or counter clock-wise)

