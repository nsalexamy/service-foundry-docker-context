# Dockerfile for running Java application with OpenJDK 21
# This Dockerfile is supposed to be placed in the build/libs directory
# Use OpenJDK 21 as base image
FROM openjdk:21-jdk-bullseye
COPY ./nsa2-otel-exporter-0.0.1-SNAPSHOT.jar /usr/app/nsa2-otel-exporter.jar
WORKDIR /usr/app
EXPOSE 4318
EXPOSE 9464
#EXPOSE 8081
ENTRYPOINT ["java", "-jar", "nsa2-otel-exporter.jar", "--spring.cloud.bootstrap.enabled=true", "--server.port=4318"]
#ENTRYPOINT ["java", "-jar", "nsa2-configwatcher-client-example-0.0.1-SNAPSHOT.jar", "--spring.cloud.bootstrap.enabled=true", "--spring.cloud.kubernetes.secrets.paths=/etc/secrets"]
