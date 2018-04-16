FROM java:8-jre
MAINTAINER QjeX <theqjex@gmail.com>

ADD ./build/exec.sh /srv/exec.sh
ADD ./build/snake.jar /srv/snake.jar

RUN mkdir /srv/data

WORKDIR /srv

VOLUME ["/srv/data"]

ENTRYPOINT ["/srv/exec.sh"]
