MAVEN WEB PROJECT WITH DOCKER

Folder structure:
maven-docker-web/
  pom.xml
  Dockerfile
  src/
    main/
      webapp/
        index.jsp

Requirements:
- Docker Desktop installed and running.

Run these commands in PowerShell from this folder:

1. Build the Docker image:
   docker build -t maven-web-app .

2. Run the container:
   docker run -d --name maven-web-container -p 8084:8080 maven-web-app

3. Check the container:
   docker ps

4. Open the application:
   http://localhost:8084

5. View logs:
   docker logs maven-web-container

To stop:
   docker stop maven-web-container

To start again:
   docker start maven-web-container

If the container name is already in use, remove the old container first:
   docker rm -f maven-web-container
