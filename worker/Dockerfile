FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder
WORKDIR /worker
COPY . /worker
RUN mvn dependency:resolve
RUN mvn package

FROM eclipse-temurin:21-jre-alpine
COPY --from=builder /worker/target/worker-jar-with-dependencies.jar .
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]