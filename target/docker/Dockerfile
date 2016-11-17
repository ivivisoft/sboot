FROM frolvlad/alpine-oraclejdk8:slim
MAINTAINER Andy Zhang (A.Z.) <ivivisoft@gmail.com>
VOLUME /tmp
ADD ivivisoft-1.0-SNAPSHOT.jar app.jar
RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS="-agentlib:jdwp=transport=dt_socket,address=5005,server=y,suspend=n"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/urandom -jar /app.jar" ]