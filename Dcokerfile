# For Java 8, try this 
FROM openjdk:8-jdk-alpine 
# For Java 11, try this 
FROM adoptopenjdk/openjdk11:alpine-jre

ARG JAR_FILE=target/spring-boot-2-hello-world-1.0.2-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","app.jar"]
