# From maven with java 11 prebuilt image
FROM maven:3.6.3-openjdk-11-slim AS build

RUN mkdir -p /workspace

WORKDIR /workspace

COPY pom.xml /workspace

COPY src /workspace/src

# create a jar file inside /target
RUN mvn -B package --file pom.xml

FROM openjdk:11-slim

COPY --from=build /workspace/target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]