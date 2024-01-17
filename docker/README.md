# About

# Cmd
"list image"
docker images

"list containers"
docker ps -a

"container creation"
docker run --name ?? ubuntu:18.04
docker run --name ?? -ti ubuntu:18.04

"container creation w/ host com bind"
docker run --name ?? -ti -v <host directory>:/mnt <IMAGE_NAME>:<TAG>

"container removal"
docker container rm <CONTAINER_NAME>

"container stop"
docker stop <CONTAINER_NAME>
	
"image removal"
docker rmi <IMAGE NAME>:<TAG>
	
docker attach  <CONTAINER_NAME>
docker start  <CONTAINER_NAME>

"docker image commit"
docker commit -m "imitial commit" <CONTAINER_NAME> <IMAGEA_NAME>:<CUSTOM TAG>

"limit host computer's resource"
i.e) docker run -ti --memory="1g" ubuntu:18.04

"show stats"
docker stats <CONTAINER_NAME> 
	
ctrl d -> terminate container
