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


### **Course Explanation: Obstacle Avoidance & Navigation**

The code begins by establishing where all the physical components like motors, sensors, and camera are connected. It also sets important constants that act as the robot's rules of operation:

*   **Max Sequences:** Dictates the total number of times the robot will perform a primary color detection and turn sequence. When it reaches this number, the robot will shut down.
*   **Color Detection Pause:** A 6-second period after detecting a blue or orange line where the robot ignores further blue/orange detections. This ensures it completes its turn and reverse maneuver without being interrupted. During this pause, it can still detect and react to red and green obstacles.
*   **Steering Angles:** The robot uses two sets of turning angles. **Sharp turns** are used during the initial setup and for quick ultrasonic obstacle avoidance. **Mild turns** are used for the main course navigation, providing smoother and more controlled turns around obstacles and after detecting lines.
*   **Ultrasonic Threshold:** The minimum distance, in centimeters, at which the robot considers an object an obstacle and will initiate an avoidance turn.

*   **Sensors & Perception:**
    *   The robot relies on two main sensing systems that work together:
        *   **HuskyLens Camera:** This is the primary sensor for navigation. It is trained to recognize four colors:
            *   **Blue & Orange:** These are the *primary navigation lines*. They signal the robot to execute a turn sequence, bump into the wall behind it, and then continue, effectively moving it to the next section of the course.
            *   **Red & Green:** These act as *virtual obstacles*. When detected, the robot performs an avoidance maneuver by backing up and turning left and right to navigate around them.
        *   **Ultrasonic Sensors:** These act as a secondary, physical safety system for obstacle avoidance. If the robot gets too close to a wall or object on its left or right side, these sensors will command a mild turn to keep it centered and avoid crashes.

*   **Startup Sequence:**
    *   When powered on, the robot initializes its motors, servo, and sensors.
    *   It performs an initial environmental check using the ultrasonic sensors to ensure it has space to operate.
    *   It then checks for the HuskyLens camera and prepares it for color detection.

*   **Main Operation Loop:**
    *   The loop constantly checks a specific order of events:
        1.  **Shutdown Check:** It first checks if the maximum number of sequences has been reached to begin the shutdown process.
        2.  **Continuous Ultrasonic Monitoring:** The ultrasonic sensors are the least importnat part of the code. If a wall is detected, the robot turns mildly away from it, and then continues forward. This in done top avoid walls in case Cap. gets to close to them. This is vital to ensure the HuskyLens has a clear vieww of all the obtsacles. If its to close to one side, its posible he'll miss the detctio of certain obstacles. 
        3.  **Color Detection & Reaction:** The robot simultaneously looks for colors. He has to given instruction in case he detcts one of the two possible sets of colors:
            *   **Blue/Orange:** The robot will continue a forward motion for a few seconds loneger, sort of a delay before turning. This is so that he has advanced enough to turn and bump into the walll behind him. He first turns in the corresponding direction, then reverses to bump into the wall. This way, he can always center himself and is awa.re of all the onjevts in front of him. This preventes him from turning too sharply or too wideley and missing obstacles around him. When completing this sequence, he also tallies it up so as to keep track of how many laps are missing. Once he reaches 12, he will stop. Lastly, after the detection of one of the colored lines, he enters a pause period where it ignores further blue/orange lines so as to not detect the same line when going forward again.
            *   **Red/Green:** This feature allows him to avoid obstacles. When detcting either green or red, he stops, reverses briefly so as to not bump into the obstacle, and then performs a sequenced turn (left-then-right or right-then-left) to navigate around the virtual obstacle before continuing forward. When he makes thsi maneuver he ensures the obstacle is avoided, but also places hinmslef back in his path. 

*   Once the robot completes its maximum number of sequences, it stops its motor, bringing the course run to a complete end.
