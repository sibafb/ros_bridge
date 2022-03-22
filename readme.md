# How to Use

- [Bridge](#Bridge)
- [Web Server](#WebServer)

## Bridge

### server
- setting
  if you using docker, set port forwarding option.
  (9090 port is dafault.)
  ```
  docker run -p 9090:9090
  ```

- install

  ```
  sudo apt-get install ros-$ROS_DISTRO-rosbridge-suite
  ```

- launch 

  ```
  roslaunch rosbridge_server rosbridge_websocket.launch
  ```

### client
- install

  melodic
  ```
  curl -kL https://bootstrap.pypa.io/pip/2.7/get-pip.py | sudo python
  ```
  ```
  sudo pip install roslibpy
  ```

  ```
  sudo pip install service_identity
  ```

- edit 
  set ip adress in ros_bridge_client.py
  ```python 
  self.ros_client = Ros('192.168.XXX.XXX', 9090)
  ```



## WebServer

- install
  ```
  sudo apt-get install ros-$ROS_DISTRO-roswww
  ```
- launch
  ```
  roslaunch ros_bridge bridge.launch
  ```
- access 
  - open beowser and access http://localhost:8085/ros_www_sandbox/pub_goal_and_stop.html
  - "ros_bridge" is Package name. If you changed that, follow it.



- 

## Reference
### server
- [ROS Wiki Running Rosbridge](http://wiki.ros.org/rosbridge_suite/Tutorials/RunningRosbridge)


### client libraries
- [roslibpy](https://roslibpy.readthedocs.io/en/latest/examples.html)

- [roslibjs](http://wiki.ros.org/roslibjs)
- [roslibjsの基本的な使い方](https://qiita.com/daigakupotato/items/bb44c070d4304caa4bf1)

## 使い方
