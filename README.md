# RUN ROS2 SERVER NODE & CLIENT NODE IN DOCKER

## Requirement
a. Install Docker
https://docs.docker.com/engine/install/ubuntu/

b. Install ros2 Humble
https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html


## Set Up Environment

1.git clone this repo

```
$ git clone https://github.com/bleeze57/ros2Docker.git
```

2.Change directory to "ros2_root"
```
  $ cd ros2_root
```

3.Build Docker image
```
  $ docker build -t ros2docker .
```

4.Check created docker image
```
  $ docker images
```

5.Run Docker image
```
$ docker run -it --rm ros2docker
```

6.your user will change into docker, open another terminal and check docker runnin image
```
$ docker ps
```
## Run Server Node & Client Node
1. Go bakc to the docker terminal, run the ros package
