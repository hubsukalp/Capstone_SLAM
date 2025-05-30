<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/cover.png">
</div>

### Goal
The project aims to develop a comprehensive robotic system capable of autonomous navigation. This includes designing a feedback controller to regulate motor speed and a velocity-based movement controller, implementing 2D mapping using Lidar for simultaneous localization and mapping (SLAM), and constructing a path planner for effective navigation within the mapped environment.


## System setup
- [Set up Jetson Nano System](https://drive.google.com/file/d/1snBIfBYC1WnWeXmGDQzVPnzadDBNNSKM/view?usp=sharing) 
- [Update System Utilities](https://drive.google.com/file/d/1JjxOLtd89kO1biE8RGukBOlJu6GlabRv/view?usp=sharing)
- [Set up MBot firmware](https://drive.google.com/file/d/1uhqe8_y8aP5RM1-PqLhodTnwgl3P1jzo/view?usp=sharing)
- [Install the rest of the MBot Code](https://drive.google.com/file/d/1TBajTu7aj07esqkXXomnzD3DQJbb_Vxi/view?usp=sharing)

## Communication framework
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/mbot_communication.png">
</div>

## Results

### Wheel speed calibration (PWM-speed linear mapping)
- This is the core of our open-loop wheel speed controller while also used in the closed-loop wheel speed controller
<!-- <div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/pwm_mapping.png">
</div>  -->
<!-- <div style="display: flex;">
  <div style="margin: 10px;">
    <img style="max-width: 30%; height: auto;" src="assets/left_motor.png" alt="left_motor">
  </div>
  <div style="margin: 10px;">
    <img style="max-width: 30%; height: auto;" src="assets/right_motor.png" alt="right_motor">
  </div>
</div> -->
<div style="text-align: center;">
  <img src="assets/left_motor.png" alt="left_motor" style="display: inline-block; width: 65%; margin: 0; padding: 0; border: none;"/>
  <img src="assets/right_motor.png" alt="right_motor" style="display: inline-block; width: 65%; margin: 0; padding: 0; border: none;"/>
</div>


### Motion control
- Mbot's motion control is composed of 3 hierarchical levels as shown below:
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/motion_controller.png">
</div> 
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/velocity_controller.png">
</div> 
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/wheel_speed_controller.png">
</div> 

- Closed-loop Wheel speed PID controller (showing step input response)
<!-- <div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/pid_response.png">
</div>  -->
<!-- <div style="display: flex;">
  <div style="margin: 10px;">
    <img style="max-width: 30%; height: auto;" src="assets/left_wheel_pid_response.png" alt="left_wheel_pid_response">
  </div>
  <div style="margin: 10px;">
    <img style="max-width: 30%; height: auto;" src="assets/right_wheel_pid_response.png" alt="right_wheel_pid_response">
  </div>
</div> -->
<div style="text-align: center;">
  <img src="assets/left_wheel_pid_response.png" alt="left_wheel_pid_response" style="display: inline-block; width: 65%; margin: 0; padding: 0; border: none;"/>
  <img src="assets/right_wheel_pid_response.png" alt="right_wheel_pid_response" style="display: inline-block; width: 65%; margin: 0; padding: 0; border: none;"/>
</div>

- Mbot Velocity controller response (when driven on an oval track)
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/vel_controller.png">
</div> 

### SLAM (Simultaneous Localization & Mapping)
- SLAM Components (Monte Carlo localization & Occupancy grid-based mapping)
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/slam_components.png">
</div> 

- Demo
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/mbot_slam_gif.gif">
</div> 

### Path Planning 
- Demo using A* algorithm
<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="assets/bot_a_star_gif.gif">
</div> 
