# Этап 1: сборка
FROM openjdk:8-jdk-alpine AS build

WORKDIR /app

COPY .mvn/ .mvn
COPY mvnw pom.xml ./
RUN chmod +x mvnw


RUN ./mvnw dependency:go-offline

RUN printenv

COPY src ./src

RUN ./mvnw clean package -DskipTests

FROM openjdk:8-jdk-alpine

WORKDIR /app


COPY wait-for-it.sh /app/wait-for-it.sh
RUN chmod +x /app/wait-for-it.sh


COPY target/*.jar /app/app.jar
RUN apk add --no-cache bash

EXPOSE 8086

# Команда запуска с ожиданием доступности PostgreSQL на хосте postgres:5432
CMD ["bash", "./wait-for-it.sh", "my-postgres-db:5432", "--", "java", "-jar", "/app/app.jar"]