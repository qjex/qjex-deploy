FROM anapsix/alpine-java:8

MAINTAINER QjeX <theqjex@gmail.com>

ADD ./build/*.jar /srv/app.jar
ADD ./build/run.sh /srv/run.sh
ADD ./build/config.properties /srv/config.properties
ADD ./build/rules.txt /srv/rules.txt

WORKDIR /srv
ENTRYPOINT ["sh", "run.sh"]