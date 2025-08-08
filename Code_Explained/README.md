## Open Challenge Programming

Our open challenge programming works by establishing a variable for the two values of the lateral ultrasonic sensors and then creating a time variable that ends once the robot has completed its course. Our robot completes the course in an approximate time of **90s**, this means that once the time passes, the rear axle's motor value is set to zero and our robot stops. A conditional is added in which if the distance of both ultrasonic sensors is greater than **45cm**, then the front steering goes straight. Then, if the distance between the left sensor is less than **50cm** and greater than zero, the servo in our steering will move right by being set on **210°** and pause for **200ms**. The same happens with the right ultrasonic sensor, if the distance between the right sensor is less than **50cm**, then the servo will move to **150°**, this will cause it to move left, and then pause for **200ms** the same way it happened with the left sensor.


## Programming Challenge Obstacles

Although for this regional we weren't able to complete the programming for the obstacle course, we plan to incorporate it further along. We will use a **HuskyLens camera** that is capable of identifying colors and objects and storing the information in its database. The stored data will be implemented into the programming so as to steer clear of obstacles by indicating the color of the object, and then moving either left or right accordingly.
