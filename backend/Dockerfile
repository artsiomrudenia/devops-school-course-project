# Use a base image with Java 8 installed
FROM openjdk:8-jdk-alpine

# Install PostgreSQL client tools and curl
RUN apk update && \
    apk add --no-cache postgresql-client curl

# Set the working directory inside the container
WORKDIR /app

# Copy the built JAR file into the container
COPY build/libs/dev-school-app-1.0-SNAPSHOT.jar /app/

# Expose the port the application runs on
EXPOSE 8080

# Command to run the application
CMD ["java", "-jar", "dev-school-app-1.0-SNAPSHOT.jar"]

