# ISV & DN COE Intro to Containers Repo

## This Repo is a holding repo for the "Intro to Containers" How to Series

### Docker Commands Used In Intro Series

```bash
docker version
docker search busybox
docker pull busybox/docker images
docker run busybox ls
docker ps
docker ps -a

docker run -it ubuntu /bin/bash
docker run -itd ubuntu
apt-get update -y
apt-get install -y iputils-ping

//utility commands to use
docker stop $(docker ps -a -q)
docker ps -aq | xargs docker stop | xargs docker rm
docker ps -aq | xargs docker rm -f

docker ps/docker stop container_id
docker start container_id/docker ps
docker ps/docker rm  -f  container_id

touch dummy.txt/docker run -itd ubuntu/docker cp dummy.txt container_id:/root/
docker run -itd ubuntu/docker container cp containerId:/path/file /path/on/localmachine
docker ps/docker exec -it container_id bash
docker run -itd ubuntu/docker ps/docker inspect container_id

docker run -itd nginx/docker ps/docker logs container_id
docker run -itd ubuntu/docker ps/docker kill container_id

docker pull httpd/docker save httpd > httpd.tar
docker image load < httpd.tar
docker run -itd ubuntu/docker ps/docker stats container_id
docker run -itd ubuntu/docker ps/docker top container_id
docker run -itd nginx/docker ps/docker restart container_id
docker run -itd nginx/docker ps/docker rename old_name new_name
docker run -itd -p 80:80 nginx/docker ps

docker images
docker inspect ubuntu
docker rmi -f ubuntu
docker image prune
docker history ubuntu

//docker networking
docker network ls
docker network inspect bridge
docker network create intronetwork
docker container run -itd --network=intronetwork ubuntu
docker network disconnect network_name container_name
docker container run -itd --network host ubuntu
docker network rm intronetwork
docker network prune
docker run -d --name web1  -p 8001:80 nginx
docker run -d --name web2  -p 8002:80 nginx
docker run -d --name web3  -p 8003:80 eboraas/apache-php
docker run -d --name web4  -p 8004:80 eboraas/apache-php
docker network connect intronetwork web1
docker network connect intronetwork web2
docker network connect intronetwork web3
docker network connect intronetwork web4

docker exec -ti web1 ping web2

//docker volumes
docker volume ls
docker volume create introvol/docker volume ls
docker run -itd -p 8080:8080 -v introvol:/var/jenkins_home jenkins:2.60.2
docker run -p 9090:9090 -v /PATH/TO/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus
docker kill container_id/docker rm contaner_id/docker volume rm myvol
docker volume prune

docker container run -itd -p 8080:8080 -v /tmp:/var/jenkins_home jenkins:2.60.2

//install Portainer
docker run -d -p 8000:8000 -p 9443:9443 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
https://localhost:9443/
user:admin
password:introtocontainers


```
