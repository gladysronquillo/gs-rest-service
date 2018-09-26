# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

# Maintener
MAINTAINER Gladys Ronquillo <gladysronquillo@outlook.com>

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 8080 available to the world outside this container
EXPOSE 8080

# The application's jar file
ARG JAR_FILE=target/gs-rest-service-0.1.0.jar

# Add the application's jar to the container
ADD ${JAR_FILE} gs-rest-service.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/gs-rest-service.jar"]

# Proceso ha realizar:
# dirigirse al path /complete
# crear el archivo .jar ejecutando el sigueinte comando en el cmd (usando maven): mvnw package && java -jar target/gs-rest-service.jar
# creación de la imagen, ejecutar: docker build -t spring .
# creación del contenedor, ejecutar: docker run -p 5000:8080 --name=gs-rest-service -d spring
## referncia https://spring.io/guides/gs/rest-service/
## https://spring.io/guides/gs/spring-boot-docker/
## Proyecto en intelligen ide https://docs.microsoft.com/en-us/java/azure/intellij/azure-toolkit-for-intellij-publish-spring-boot-docker-app?view=azure-java-stable