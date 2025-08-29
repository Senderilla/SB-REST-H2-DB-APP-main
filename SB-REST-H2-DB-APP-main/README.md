# SB-REST-H2-DB-APP
SONARQUBE CODE CHECK

# Steps to Build and Deploy the Container
# Build the Maven Project Locally: Run the Maven build process on your local machine to create the target directory with the built JAR file:
mvn clean package -DskipTests

# This command will generate the JAR file inside the target folder:
$ target/Africa-United-App-0.0.1-SNAPSHOT.jar

# Build the Docker Image: Use the updated Dockerfile to build the Docker image. Make sure you're in the project root directory (where target exists):
$ docker build -t africa-united-app .

# Run the Docker Container: Start the container and map port 8080 from the container to your local machine:
docker run -d -p 8080:8080 --name africa-united-app africa-united-app

# Verify the Application: Access the application using a browser or API client:
http://localhost:8080

# Stop and Remove the Container: If you need to stop and remove the container:
docker stop africa-united-app
docker rm africa-united-app
