
# IMU SENSOR FUSING 
## How to Configure IMU_Sensor with Raspberry PI and Publishing IMU_Data over ROS2 Topic

This setup shows how you can connect the bno055 (IMU_Sensor) with Raspberry Pi and Publishing the data over the ROS2 Topic.
#### IMU - Intertial Measurement Unit is a type of Sensor used to Triaxial Acceleration and Rotational Measurements. In this Setup bno055 (by Bosch) is used which is absolute type Sensor. This is used for collecting Odometry Data which is later combined with Lidar or Camera or both to generate Maps and Navigation. This Sensor is connected to Raspberry Pi5 model (hosting Ubuntu Desktop)

#### Components Used in this Setup
1.bno055 IMU_Sensor : [Purchase Link](https://thinkrobotics.com/products/9-dof-absolute-orientation-bno055-sensor?variant=40115292405846&country=IN&currency=INR&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&utm_source=googleads&utm_medium=cpc&gad_source=1&gclid=CjwKCAiA34S7BhAtEiwACZzv4T9hiuFVUXhk3RKVSjYI5AnG5UfELxI5eGd4oA_c2BmAvBLoU2u8mRoC6gEQAvD_BwE)

2.Raspberry Pi5 : [Purchase Link](https://robu.in/product/raspberry-pi-5-model-8gb/?gad_source=1&gclid=CjwKCAiA34S7BhAtEiwACZzv4Te7ZsV72q4ZIZ2xwZzbUdkEw_dp_BJ75tgewU_Puo9fhUbit706HhoC-2MQAvD_BwE)

### The Circuit Diagram of this setup is shown as below
![image](https://github.com/user-attachments/assets/effbd9d6-7d74-41f7-bae4-6a3d9a2090ec)

#### 1. clone the repository
```
git clone https://github.com/holmes24678/IMU_Node
```
#### 2.Build the workspace
```
colcon build 
```
#### 3. Run the IMU_Node
```
ros2 run bno055_publisher_python bno055_publisher
```
![image](https://github.com/user-attachments/assets/20aecc18-76ca-49a7-aca8-ac56c239bc95)

#### 4. Echo the message over Topic
```
ros2 topic echo /bno055/imu
```
![image](https://github.com/user-attachments/assets/1898a918-5dba-4fc5-a529-e2e6999f9de6)


Thanks for Coming for any clarifications contact me hsherlock366@gmail.com

