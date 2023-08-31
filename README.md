# ROS2_my_robot

## 소개
- URDF(Unified Robot Description Format, 로봇 기술용 통일 포맷)란?
- 로봇을 구현하는데 사용되며, Navigation, Manipulation, Remote Control 등이 가능하며, 기본적으로 XML문법을 통해 만들어짐.
- 작성된 코드는 URDF를 통해 직접 로봇을 디자인하고, 물리적인 요소들을 적용하여 GAZEBO simulation 안에서 움직일 수 있도록 구현한 코드입니다.
- my_robot_description 패키지 안에서 관련 항목들을 찾아볼 수 있습니다.
- 로봇 모델에 lidar, camera 센서가 부착되어 있습니다.

#### [환경]
|목록|VERSION|
|:--|:--:|
|Ubuntu|Ubuntu 20.04.6 LTS (Focal Fossa)| 
|ROS|Galactic Geochelone| 

## 실행 코드 
### 00_사전 설정
```python
sudo apt update
sudo apt install ros-galactic-joint-state-publisher-gui  # joint-state-publisher-gui 패키지 설치
sudo apt install ros-galactic-xacro  # xacro 패키지 설치
sudo apt install ros-galactic-gazebo*  # gazebo simulation 관련 모든 패키지 설치
```
### 01_display.launch.py
```python
# rviz2에서 로봇의 모형 및 tf 확인
ros2 launch my_robot_description display.launch.py
```
### 02_launch_sim.launch.py
```python
# rviz2에서 로봇의 모형 및 tf 확인
ros2 launch my_robot_description launch_sim.launch.py
# 추가적으로 로봇을 키보드로 움직일 수 있는 명령어
ros2 run teleop_twist_keyboard teleop_twist_keyboard 
```
## 실행 결과
### 01_display.launch.py
![display.launch.py](https://github.com/SaltnLight-pet/ROS2_my_robot/assets/142612336/39f2c833-0161-4c96-9206-e6fbc3ba436a)
### 02_launch_sim.launch.py

