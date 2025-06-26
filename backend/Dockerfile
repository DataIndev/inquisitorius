FROM openjdk:17-jdk-slim
WORKDIR /app
# Given permissions to mvnw
RUN ./backend/mvnw clean package -DskipTests

COPY target/*.jar app.jar
EXPOSE 3000

ENTRYPOINT ["java", "-jar", "app.jar"]

