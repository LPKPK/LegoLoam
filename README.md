# Lego-Loam



## Quick start
[Download](https://drive.google.com/file/d/11lYeENSYiwqLT3WJK8DymWcJKXYoiv-L/view?usp=sharing) campus dataset

```
roslaunch  lego_loam run.launch
rosbag play campus_isec.bag -r 2 --clock   --topic  /ns1/velodyne_points   /imu/imu
```

## IMU Alignment
Because the corrected by the IMU data is based on the sensor motion, the best way to use IMU data as corrected input is that make sure your IMU is aligned with the lidar properly before you collect your own dataset. If not, you should change transfer the IMU frame to "base_link". Like the way we did. In our cars, the IMU frame and the Lidar frame are shown as below.

<img src="https://user-images.githubusercontent.com/51788243/170725229-5c6bf6e8-3f32-47b4-95fa-f04c07708513.jpg" width="700">



***

