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
## docker-compose 명령어
> docker-compose ...
```
$ docker-compose up
```