## Open Challenge Programming

For our previous robot we programmed using MakeCode for microbit. It consisted of a simple code that would rotate the servo to 210 degrees if the left ultrasonic sensor percieved a distance less than 45cm. The same would happen with the right ultrasonic sensor, but in that case the servo will rotate to 150 degrees. In the case that both sensors read a distance greater than 30cm, the servo was set to 180 degrees and it would continue its straight path. Once the time variable ended, the DC motor would be stopped, and our robot would park in the position it started. 

Since we developed **Captain ÑomÑom**, We have now programmed a new code that includes other components that facilitate Cap.'s cruising. 

*   The code begins by establishing where all the physical components like motors and sensors are connected. It also sets important constants that act as the robot's rules of operation:

      *   **Max Sequences:** Dictates the total number of times the robot will perform  the color detection and then turn. When it reaches this number Cap. will shut down.
      *   **Reset Delay:** The brief pause the robot takes after reacting to a color before it's ready for the next one. This ensures Cap. will read only one color when he gets to the turns. Without it, he would detect both blue and orange and would turn in oppossite directions, steering him away from his course.
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


## Obstacle Challenge Programming

For the obstacle challenge we seek to achieve the 7 initial points achieved by leaving the parking area inside the two pink walls. The code for this task is fairly simple. Seeing as **Captain ÑomÑom** is small enough to take a sharp turn and leave the space without bumping into the walls, we simply add that to the beginning of our code.

We begin by establishng the values of the two ultrasonic sensor as their own variable, and then **Cap.** will detect wether he is on the left or right side of the outer wall. Once he determines this, the front steering will turn to the opposite side, and he can leave the parking spot successfully. This is true no matter the direction in which he goes (Clock-wise or counter clock-wise). 

After doing so, it will continue with a fairly similar version of the open course code. The only changes made were teh addition of two new COLOR:ID's, these represent the green and red obstacles. Once it detects either one of these variables it will turn sharply to its corresponfing side for a few seconds, and will then return on its course, making sure to keep track of the colored lines on the floor so as to complete three full rounds. Once it does this, he is not able to parallel park inside the two magenta walls. 

