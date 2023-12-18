FROM amazoncorretto:17

ARG JAR_FILE="ecmp-dev-0.0.1-SNAPSHOT.jar"

COPY target/${JAR_FILE} /app/api.jar

ENTRYPOINT ["java","-jar", "/app/api.jar"]