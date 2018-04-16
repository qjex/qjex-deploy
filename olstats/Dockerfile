FROM anapsix/alpine-java:8
MAINTAINER QjeX <theqjex@gmail.com>

ADD ./build/*.jar /srv/app.jar
ADD ./build/config.properties /srv/config.properties

WORKDIR /srv
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/srv/app.jar"]
