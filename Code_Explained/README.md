## Open Challenge Programming

For our previous robot we programmed using MakeCode for microbit. It consisted of a simple code that would rotate the servo to 210 degrees if the left ultrasonic sensor percieved a distance less than 45cm. The same would happen with the right ultrasonic sensor, but in that case the servo will rotate to 150 degrees. In the case that both sensors read a distance greater than 30cm, the servo was set to 180 degrees and it would continue its straight path. Once the time variable ended, the DC motor would be stopped, and our robot would park in the position it started. 

Since we developed **Captain ÑomÑom**, We have now programmed a new code that includes other components that facilitate Cap.'s cruising. 

*   The code begins by establishing where all the physical components like motors and sensors are connected. It also sets important constants that act as the robot's rules of operation:

      *   **Max Sequences:** Dictates the total number of times the robot will perform  the color detection and then turn. When it reaches this number Cap. will shut down.
      *   **Reset Delay:** The brief pause the robot takes after reacting to a color before it's ready for the next one. This ensures Cap. will read only one color when he gets to the turns. Without it, he would detct both blue and orange and would turn in opssite directions, steering him away from his course.
      *    **Shutdown Delay:** The amount of time the robot waits after its final sequence before turning off its motor. With this fuction, we can ensure Cap. reaches it original position and doesnt stop suddenly in the middle of a turn.
      *  **Steering Range:** The servo motor's movement is limited to a safe range where we have the MAX and MIN angles, 108 and 78 degrees accordingly, to prevent the robot from making overly sharp turns. 

*   **Sensors & Perception:**
    *   The robot relies on two main sensing systems that work together:
        *   **HuskyLens Camara:** This is the primary component of the code. It is trained to recognize organge and blue to perform the turns and not rely solely on ultrasonic sensors. When it detects blue, it commands a left turn. When it detects oragne, it commands a right turn.
        *   **Ultrasonic Sensors:** These act as a secondary system for obstacle avoidance. If Cap. gets too close to a side of the walls, the ultrasonic sensors will help him stay centered, and avoid crashing. 

*   **Startup Sequence:**
    *   When powered on, the robot pauses for 3 seconds to ensure all systems are ready.
    *   It then checks for the HuskyLens camera and prepares it for color detection.

*   **Main Operation Loop:**
    *   The core of the code is a loop that constantly checks a specific order of events:
        1.  **Shutdown Check:** It first checks if the maximum number of sequences has been reached to begin the shutdown process. This number is 12, seeing as Cap. would need to detect the color 12 times in order to complete three full rounds. 
        2.  **Color Detection:** If it hasn't reached the max number of sequences (12 detections), it prioritizes looking for the colored lines. When a color is spotted, it executes the corresponding turn, atllies up the sequence, and temporarily pauses further color detection for 2 seconds.
        3.  **Obstacle Avoidance:** While paused for color detection (or when no color is seen), the ultrasonic sensors remain active to avoid bumps.
        4.  **Reset:** After the reset delay, the robot centers its wheels and resumes looking for colors, continuing the cycle until its task is complete.


* Once it completes the three rounds the servo is set back to 90 degrees so that it will go straight for a few seconds more and park in its original position bringing us to the end of our Open Course Code. 

 
|---|

Our open challenge programming works by establishing a variable for the two values of the lateral ultrasonic sensors and then creating a time variable that ends once the robot has completed its course. These variables are set as "sensor derch." (Right sensor), and "sensor izq." (Left sensor), so as to facilate the understanding of our code. 

Our robot completes the course in an approximate time of **90s**, this means that once the time passes, the rear axle's motor value is set to zero and our robot stops.

A conditional is added in which if the distance of both ultrasonic sensors is greater than **45cm**, then the front steering goes straight and pauses for **200ms**. If the distance between the left sensor is less than **50cm** and greater than zero, the servo in our steering will move right by being set on **210°** and pause for **200ms**. The same happens with the right ultrasonic sensor. If the distance between the right sensor is less than **50cm**, then the servo will be set to **150°**, this will cause it to move to the left, and then pause for **200ms** the same way it happened with the left sensor.

This code allows our robot **POP** to achieve 30 points consistently, since its able to go aorund the track 3 times, then park succesfully without coming into contact with any of the inner or outer walls. This is true for every starting position. 

## Obstacle Challenge Programming

For the obstacle challenge we seek to achieve 7 points by leaving the parking area inside the two pink walls. The code for this task is fairly simple. Seeing as **POP** is small enough to take a sharp turn and leave the space without bumping into the walls, we have a shortned version of our code for the open challenge. 

We begin by establishng the values of the two ultrasonic sensor as their own variable, and then **POP** will detect wether he is on the left or right side of the outer wall. Once he determines this, the front steering will turn to the opposite side, and he can leave the parking spot successfully. This is true no matter the direction in which he goes (Clock-wise or counter clock-wise)

