
# Razor-IMU-9DOF

Repo for 9DoF Razor IMU M0 calibration




## Steps

Clone the project

```bash
  git clone https://github.com/SeeramRoboticist/Razor-IMU-9DOF.git
```
- create a workspace and build the package inside it.
- follow this link https://learn.sparkfun.com/tutorials/9dof-razor-imu-m0-hookup-guide/all and upload the Razor_AHRS.ino to ardiuno.

- use this link to callibrate accelerometer and gyroscope https://wiki.ros.org/razor_imu_9dof

- try running the below command
```bash
  roslaunch razor_imu_9dof razor-pub-and-display.launch
```

- use my code if you get errors while running above launch file, because ros wiki or other repo are of older version.

- you will see yaw drift when you test the code.

- To resolve the yaw issue, you have to install process and ejml 0.23 first.
- once installed, in imu folder in my repo, razor_imu_9dof/imu/razor-9dof-ahrs/Processing/Magnetometer_calibration/Magnetometer_calibration.pde run this code using process.

- move your imu up down however you want and see there should be a points gathered together. hit "space button" you will get output values.

## Warning

- we have callibrated all the 3 sensors now and updated in the .ino file but we have to update all the callibrated values in the **my_razor.yaml**.

- now run the below command once again,
```bash
  roslaunch razor_imu_9dof razor-pub-and-display.launch
```

- thats it we have callibrated the sensors

- if you have any furter quries mail me seeramroboticist@gmail.com

