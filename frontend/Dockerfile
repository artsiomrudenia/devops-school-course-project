# Use a base image with Java 8 installed
FROM openjdk:8-jre-alpine

# Install PostgreSQL client tools and curl
RUN apk update && \
    apk add --no-cache postgresql-client curl

# Set the working directory inside the container
WORKDIR /app

# Copy build files from the Gradle output directory to the Nginx web server directory
COPY ./devschool-front-app-server/build/libs/devschool-front-app-server-1.0.0.jar /app/

# Expose port 8081 to the outside world
EXPOSE 8081

# Specify the command to run your application
CMD ["java", "-jar", "devschool-front-app-server-1.0.0.jar"]