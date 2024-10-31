# by default docker command it will check for docker file 

# Docker Image 
* base os +  run time + system packages and application depends + application code 

# Installing docker 
```shell
sudo yum install -y yum-utils
```
```shell
sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo -y
```
```shell
 sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```

```shell
usermod -aG docker ec2-user
```

* exit and login again 

```shell
sudo systemctl start docker
```
* how to run a container in 
```shell
docker run -d -p 80:80 nginx
```
###  `run` = pull + create + start
`run` command is used to run a new container
`-d` is used to run the container in detached mode
`-p` is used to map the port of the host to the port of the container

* how to check the running containers
```shell
docker ps
```
* how to check the all containers
```shell
docker ps -a
```

* docker logs
```shell
docker logs <container_id>
```
* docker running logs
```shell
docker logs -f <container_id>
```
* how to inspect container logs
```shell
docker inspect <container_id>
```


* how to access the running container
```shell
docker exec -it <container_id> bash
```


* docker stop
```shell
docker stop <container_id>
```
* how to remove a container
```shell
docker rm <container_id>
```
* how to build a docker image
```shell
docker build -t <image_name> .
`
- local format
    - image_name:tag

- push to  docker hub format 
  - url/username/image_name:tag

-  how to push a docker image to docker hub
    - docker login
    - docker push <image_name>
    - docker push <image_name>:<tag>
    - docker push <image_name>:latest
    - docker push <image_name>:1.0