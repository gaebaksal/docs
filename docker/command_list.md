# 도커 명령어 리스트

## 도커 명령어
> $ docker ...

### Docker image
```
# 이미지 받아오기
$ docker pull IMAGE_NAME

# 이미지 리스트
$ docker images

# 이미지 삭제
$ docker rmi -f [USER_IMAGE_NAME or ID]
```

### Docker Container
```
# 실행 중인 컨테이너 확인
$ docker ps

# 모든 컨테이너 확인
$ docker ps -a

# 컨테이너 삭제하기
$ docker rm -f [USER_CONTAINER or ID]
```

### Tips
```
# 모든 컨테이너 종료 및 삭제
$ docker rm -f $(docker ps -a -q)
```

---
## Docker-compose 명령어
> docker-compose ...
```
$ docker-compose up
```

---
## Docker Swarm 명령어
> docker swarm은 docker 1.12 버전부터 swarm mode로 합쳐짐.

### docker swarm
```
# 해당 서버를 매니저 노드로 실행
$ docker swarm init --advertise-addr IP

# 워커 노드가 swarm에서 떠나기
$ docker swarm leave

# 마스터 노드가 swarm에서 떠나기
$ docker swarm leave --force
```
### docker node
```
# 매니저 노드에서 워커 노드 확인하기 
$ docker node ls

# 마스터 노드에서 자식 노드 보내기
$ docker node rm HOSTNAME
```