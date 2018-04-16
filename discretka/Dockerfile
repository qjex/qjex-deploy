FROM anapsix/alpine-java:8

MAINTAINER QjeX <theqjex@gmail.com>

ADD ./build/*.jar /srv/app.jar
ADD ./build/run.sh /srv/run.sh

WORKDIR /srv
ENTRYPOINT ["sh", "run.sh"]