# Build a JAR File
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /home/app
COPY . /home/app/
RUN mvn -f /home/app/pom.xml clean package
# Create an Image
FROM openjdk:8-jdk-alpine
EXPOSE 5000
COPY /home/app/target/hello-world-java.jar hello-world-java.jar
ENTRYPOINT ["sh", "-c", "java -jar /hello-world-java.jar"]
