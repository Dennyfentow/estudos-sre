FROM openjdk:8-jdk-alpine
RUN addgroup -S spring && adduser -S spring -G spring
COPY start.sh target/
RUN chmod +x target/start.sh
# USER spring:spring
RUN ulimit -n 10000
ARG JAR_FILE=target/*jar
COPY target/* target/
# COPY ${JAR_FILE} target/forum.jar

# ENTRYPOINT ["java","-Dspring.profiles.active=prod","-jar","/app.jar"]
# ENTRYPOINT [ "/target/start.sh" ]

 ENTRYPOINT source target/start.sh