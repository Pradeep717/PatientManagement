FROM maven:3.8.5-openjdk-17 AS build

WORKDIR /app

COPY pom.xml .

RUN mvn dependency:go-offline -B

COPY src ./src

RUN mvn clean package -DskipTests

FROM openjdk:17-jdk AS runtime

WORKDIR /app

COPY --from=build ./app/target/patient-service-0.0.1-SNAPSHOT.jar ./patient-service.jar

EXPOSE 4000

ENTRYPOINT ["java", "-jar", "patient-service.jar"]