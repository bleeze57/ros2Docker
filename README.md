# RUN ROS2 SERVER NODE & CLIENT NODE IN DOCKER

## Requirement
a. Install Docker
https://docs.docker.com/engine/install/ubuntu/

b. Install ros2 Humble
https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html


## Set Up Environment

1. git clone this repo

```
$ git clone https://github.com/bleeze57/ros2Docker.git
```

2. Change directory to "ros2_root"
```
  $ cd ros2_root
```

3. Build Docker image
```
  $ docker build -t ros2docker .
```

4. Check created docker image
```
  $ docker images
```

5. Run Docker image
```
$ docker run -it --rm ros2docker
```

6. your user will change into docker, open another terminal and check docker runnin image
```
$ docker ps
```
## Run Server Node & Client Node
The server and client node is written in C++ and its directory is ros2_root/ ros2_ws/ src/ cpp_srvcli/ src/ add_two_ints_clients.cpp & add_two_ints_server.cpp

Go to ros2_ws and source the setup 
```
$ cd ros2_ws
$ source install/setup.bash
```
Run the server file first
```
$ ros2 run cpp_srvcli server
```
Open another terminal, run the docker again (step 5) and source the setup 
```
$ docker run -it --rm ros2docker
$ source install/setup.bash=
```
Run the client file, at the end of the command you can put any two int that you want to add
```
$ ros2 run cpp_srvcli client 30 40
```


