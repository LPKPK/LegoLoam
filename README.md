# Lego-Loam



## Quick start
[Download](https://drive.google.com/file/d/11lYeENSYiwqLT3WJK8DymWcJKXYoiv-L/view?usp=sharing) campus dataset

```
roslaunch  lego_loam run.launch
rosbag play campus_isec.bag -r 2 --clock   --topic  /ns1/velodyne_points   /imu/imu
```

## IMU Alignment
Because the corrected by the IMU data is based on the sensor motion, the best way to use IMU data as corrected input is that make sure your IMU is aligned with the lidar properly before you collect your own dataset. If not, you should change transfer the IMU frame to "base_link". Like the way we did in the launch file. In our cars, the IMU frame and the Lidar frame are shown as below.

<img src="https://user-images.githubusercontent.com/51788243/170725229-5c6bf6e8-3f32-47b4-95fa-f04c07708513.jpg" width="700">

***

## Result
<img src="https://user-images.githubusercontent.com/51788243/170731223-0d902f3a-faae-459c-8386-b3bc6d9e4b24.jpeg" width="700">

### Mapping with Loopclosure
<img src="https://user-images.githubusercontent.com/51788243/170729611-d8d7b14e-fc8e-46cd-8f69-d7ab2d6ab237.png" height="300"> <img src="https://user-images.githubusercontent.com/51788243/170730504-34e70afe-9c3c-4059-8d6b-0605584bdbfb.png" height="300">

### Mapping without Loopclosure
<img src="https://user-images.githubusercontent.com/51788243/170730971-3e760902-4b20-47a1-8691-6f64c035cecb.png" height="300"> <img src="https://user-images.githubusercontent.com/51788243/170730936-27702130-26e9-4cba-ab52-c7dd04fdc802.png" height="300">
