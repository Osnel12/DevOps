FROM maven:3.8.1-openjdk-11-slim as builder
WORKDIR /app
COPY pom.xml .
RUN mvn dependency:resolve
COPY src ./src
RUN mvn package

FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=builder /app/target/worker-jar-with-dependencies.jar .
# CMD [ "ls", "target" ]
# COPY . .
CMD [ "java", "-jar", "worker-jar-with-dependencies.jar" ]