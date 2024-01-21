# About


## Contents

I have included necessary concepts you need to know for Docker.

```bash
docker images
docker pull
docker ps
docker logs
docker run
docker start
docker exec
docker stop
docker rm
docker tag
docker build
docker push
```
[도커 팁](https://velog.io/@juunini/%EC%8B%A4%EB%AC%B4%EC%97%90%EC%84%9C-%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%8A%94-%EC%97%AC%EA%B8%B0%EA%B9%8C%EC%A7%80%EB%A7%8C-%EC%95%8C%EB%A9%B4-%EB%90%98%EB%8A%94-%EB%8F%84%EC%BB%A4-%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4)
# Commands
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
