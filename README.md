# Ursim_docker
This is an package that contains al to files for an ursim_docker docker build. 
The docker is also auto build on the DockerHub. By running the following you can download it:
```
docker pull ruben1111/ur3_sim_docker
```
The to run it:
```
docker run -p 30001:30001 -p 30002:30002 -p 30003:30003 -d --name ursim ruben1111/ur3_sim_docker:latest
```
* The -p are for port assigment to your host. 
* The --name will be the docker container name. If you run multiple, give diffrent names
* The -d is for detaching. Without it it looks like you can stop the container with ctrl+c but that doesnt always work.

### Possible problems:
The robot runs into protective stop.
Turn off the simulator by running:
```
docker stop ursim
```
and restart it. 
Ros might not be able to handle it in a nice way. 
Then just stop the launch files and rviz. 

If stuff wont stop erroring out check if you are running any left over docker containers in the background:
```
docker ps
```

### Build by yourself:

To build the docker image by yourself use the following command:
```
docker build -t  ur-sim-docker-ur3-no-gui /home/USER/WORKSPACE/ursim_docker/.
```

To run the docker you can use this command:
```
docker run -p 30001:30001 -p 30002:30002 -p 30003:30003 ur-sim-docker-ur3-no-gui 
```
The simulator itself is made by [Universal Robots&copy;](https://www.universal-robots.com/)

The simulator will not run the gui. 


