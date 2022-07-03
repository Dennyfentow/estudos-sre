FROM openjdk:8-jdk-alpine@sha256:94792824df2df33402f201713f932b58cb9de94a0cd524164a0f2283343547b

RUN addgroup -S spring && adduser -S spring -G spring

USER spring:spring

ARG JAR_FILE=target/*jar
COPY ${JAR_FILE} app.jar

ENTRYPOINT ["java","-Xms128M","-Xmx128M","-XX:PermSize=64m","-XX:MaxPermSize=128m","-Dspring.profiles.active=prod","-jar","/app.jar"]
