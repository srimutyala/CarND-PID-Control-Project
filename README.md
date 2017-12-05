# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

In this project we revisit the lake race track from the Behavioral Cloning Project. This time, however, we implemented a PID controller in C++ to maneuver the vehicle around the track!

Project considerations & requirements

The PID controller implementtaion closely follows the lecture notes where possible and improvise while dealing with the hyperparamter tuning and initilization.

Controller

The controller consists of 3 different control setups, the P, I & D.

The P or Proportinal controller's gain is proportional to the average error. In this case, we steer the car in proportional to what far it is from the center of the lane, the cross-track error (CTE).

The D or differential controller as indicated by its name responds based on the change in error. The differential controller is used heavily in motion control than process control. The P controller tends to overshoot the lane center and oscilates around it. To aviod this and to give a more smoother steer, we employ the differential control.

The I or the Integral control acts based on the total error of a unit where a higher error results in a faster correction and vice-versa. The integral controller in motion control helps achieve the car reach the center of the lane.
