# Build a JAR File
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /home/app
COPY . /home/app/
RUN mvn clean package
# Create an Image
FROM eclipse-temurin:17-jdk-alpine
EXPOSE 6000
COPY target/*.jar app.jar
ENTRYPOINT ["sh", "-c", "java -jar /hello-world-java.jar"]
