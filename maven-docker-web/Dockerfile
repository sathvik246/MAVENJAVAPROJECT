# Build the Maven WAR file
FROM maven:3.9-eclipse-temurin-17 AS build
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package

# Run the WAR file using Tomcat
FROM tomcat:10.1-jdk17-temurin
COPY --from=build /app/target/myapp.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
