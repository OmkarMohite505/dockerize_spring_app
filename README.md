## Dockerize Spring App
How to Dockerize Spring boot or Java Application
<a href="https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04">Install Docker</a>
Dockerfile
```bash
FROM openjdk:11
COPY target/meet.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```
```bash
docker build -t meet-docker.jar .
```
```bash
docker image ls
```
```
docker run -d -p 8080:8080 meet-docker.jar
```
<a href="https://www.baeldung.com/java-dockerize-app">Reference</a>
<img src="/repository/screenshots/Dockerfile.jpg"></img>
