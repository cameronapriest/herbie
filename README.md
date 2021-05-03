# Mars Rover - Herbie

Herbie is a Mars Rover built from JPL's open source rover (OSR). In fall 2020 and winter 2021 I led a team of 5 computer engineering majors aiming to advance the rover closer to an autonomous state. As the third team of students to work on Herbie, we were given the rover in a partially operational state. 

We spent the fall of 2020 planning, researching, and developing software solutions to allow multiple motion commands to be linked together and run sequentially, as opposed to one at a time. We focused on the calibration and recenter commands as well as forward, backward, and turn commands that needed to be adjusted due to inconsistencies across the wheel encoders.

In the winter, we separated into teams based on some of Herbie's subsystems - iOS app, supervisory system for movement correction, and vision system for hazard detection. As the head of the vision system, I designed, implemented, integrated, and documented a hazard detection and avoidance program using an NVIDIA Jetson TX2 and an [Intel L515 3D Lidar Camera](https://www.intelrealsense.com/lidar-camera-l515/). This process took research and testing with multiple cameras including an RGB camera, 2D Lidar, and finally the 3D Lidar; as well as a shift from Python to C++ to allow for ease of use between the Jetson TX2 and the Intel L515 as well as the opportunity for future parallelization with CUDA. The program utilizes Intel's RealSense SDK 2.0 to poll from the Lidar's datastream and return a boolean indicating a hazard or lack thereof within a certain distance (0.8 meters) in front of the rover.

I'm currently working on implementing an autonomous person following algorithm so Herbie can follow someone around based on a color worn by the person. I've used the Intel L515 Lidar Camera to allow Herbie to avoid obstacles in its path.

![alt text](https://github.com/cameronapriest/herbie/blob/main/herbie.jpg?raw=true)

Herbie's logo:

![alt text](https://github.com/cameronapriest/herbie/blob/main/herbielogo.png?raw=true)
