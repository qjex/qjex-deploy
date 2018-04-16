FROM anapsix/alpine-java:8

WORKDIR /srv
ADD config.properties /srv/
ADD app.jar /srv/


ENTRYPOINT ["java", "-jar", "app.jar"]
