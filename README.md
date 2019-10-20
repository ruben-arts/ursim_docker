# Ursim_docker
This is an package that contains al to files for an ursim_docker docker build. 

To build the docker image by yourself use the following command:
```
docker build -t  ur-sim-docker-ur3-no-gui /home/USER/WORKSPACE/ursim_docker/.
```

To run the docker you can use this command:
```
docker run -p 30001:30001 -p 30002:30002 -p 30003:30003 ur-sim-docker-ur3-no-gui 
```
The simulator itself is made by [Universal Robots&copy;](https://www.universal-robots.com/)




