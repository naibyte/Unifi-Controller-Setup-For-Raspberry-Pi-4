# Unifi-Controller-Setup-For-Raspberry-Pi-4

Official versions of MongoDB (requried for the Unifi Controller) don't work on the RPi4 because of its CPU architecture.  

However, this lad created some MongoDB docker images that are compatible with the RPi4:  
https://github.com/themattman/mongodb-raspberrypi-docker  

Follow the "How to Install" bit to get a docker image installed on the Pi. Or, here is the shorthand:  
```bash
wget https://github.com/themattman/mongodb-raspberrypi-docker/releases/download/r7.0.4-mongodb-raspberrypi-docker-unofficial/mongodb.ce.pi4.r7.0.4-mongodb-raspberrypi-docker-unofficial.tar.gz
docker load --input mongodb.ce.pi4.r7.0.4-mongodb-raspberrypi-docker-unofficial.tar.gz
docker images
```
---
Now it is ready to use in docker compose.  
Download the compose file in this repo and just do: ```docker-compose up -d```   
Then connect to your Pi over HTTPS on port 8443.
