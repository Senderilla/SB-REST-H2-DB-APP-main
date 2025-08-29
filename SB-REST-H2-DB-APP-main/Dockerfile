# Step 1: Use an official OpenJDK runtime image
FROM openjdk:8-jre

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy the built JAR file from the local machine into the container
COPY target/Africa-United-App-0.0.1-SNAPSHOT.jar app.jar

# Step 4: Expose the port your Spring Boot application listens on
EXPOSE 8080

# Step 5: Define the command to run the application
ENTRYPOINT ["java", "-jar", "app.jar"]
