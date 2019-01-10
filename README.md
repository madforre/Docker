# Docker Snippets

## 작동하는 컨테이너 안으로 들어가기
    sudo docker exec -it $CONTAINER_ID bash

## Stop container
    sudo docker stop $CONTAINER_ID

## Stop all containers
    sudo docker stop $(sudo docker ps -a -q)

## Remove all docker images
    sudo docker rmi $(sudo docker images -a -q)

## Stop and Remove all docker containers
    sudo docker stop $(sudo docker ps -a -q) && sudo docker rm $(sudo docker ps -a -q)

## Stop and Remove all docker containers + Remove all docker images
    sudo docker stop $(sudo docker ps -a -q) && sudo docker rm $(sudo docker ps -a -q) && sudo docker rmi $(sudo docker images -a -q)

## 컨테이너 실행하기

    docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]

 자주 사용하는 옵션

	-d	detached mode 흔히 말하는 백그라운드 모드
	-p	호스트와 컨테이너의 포트를 연결 (포워딩)
	-v	호스트와 컨테이너의 디렉토리를 연결 (마운트)
	-e	컨테이너 내에서 사용할 환경변수 설정
	–name	컨테이너 이름 설정
	–rm	프로세스 종료시 컨테이너 자동 제거
	-it	-i와 -t를 동시에 사용한 것으로 터미널 입력을 위한 옵션

## Reference

https://gist.github.com/dchapkine/8423980
https://subicura.com/2017/01/19/docker-guide-for-beginners-2.html