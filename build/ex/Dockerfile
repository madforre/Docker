# 어떤 이미지를 기반으로 하여 새로운 이미지를 만들지 명시
FROM ubuntu:18.04

# 이미지 제작자를 의미
MAINTAINER Madforre <madforre@gmail.com>

# 해당 명령어를 Container에 실행
RUN apt-get update && apt-get upgrade \
    apt-get install software-properties-common \
    add-apt-repository ppa:ondrej/php \
    apt-get update && apt-get install -yq \
    php7.3-fpm \
    php7.3-cli \
    php7.3-curl \
    php7.3-gd \
    php7.3-mysql \
    php7.3-mbstring \
    php7.3-xml \
    php7.3-common \
    php7.3-json \
RUN service php7.3-fpm start \
    ufw allow 'Nginx HTTP' \

# Dockerfile이 있는 폴더의 하위 폴더에 있는 파일을 Container
# 내부 아무대나로 복사 시킬 수 있다.
# 설정파일을 위치시키자!
# ADD 

# 원하는 포트를 개방한다. (허가할 PORT 입력)
EXPOSE

# /bin/sh 를 통해 다음 명령어가 실행된다.
# 해당 명령어는 Container가 실행 될 때마다 실행된다.
CMD