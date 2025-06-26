FROM openjdk:17-jdk-slim
WORKDIR /app
# Given permissions to mvnw
RUN chmod +x mvnw
RUN ./mvnw clean package -DskipTests

COPY target/*.jar app.jar
EXPOSE 3000

ENTRYPOINT ["java", "-jar", "app.jar"]

