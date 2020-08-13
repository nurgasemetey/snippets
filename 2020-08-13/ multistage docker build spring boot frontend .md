###  multistage docker build spring boot frontend 


[Multi-stage Docker build for React and Spring - The official voice of the Obeo experts](https://blog.obeo.fr/multi-stage-docker-build-for-react-and-spring "Multi-stage Docker build for React and Spring - The official voice of the Obeo experts")



[Spring Boot in a Container](https://spring.io/blog/2018/11/08/spring-boot-in-a-container "Spring Boot in a Container")


 

```
FROM node:10.15.3 as frontend
WORKDIR /frontend
COPY tkm .
RUN npm ci
RUN npm run-script build

FROM openjdk:7-jdk-alpine as build
WORKDIR /backend

# RUN  ls src/main/resources/public
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src src
RUN mkdir -p src/main/resources/public
COPY --from=frontend /frontend/build src/main/resources/public
RUN ./mvnw package -DskipTests
RUN ls target

FROM openjdk:7-jdk
COPY --from=build /backend/target/gateway-0.0.1-SNAPSHOT.jar /maven/app.jar
RUN ls -lah /maven/app.jar
CMD java -Djava.security.egd=file:/dev/./urandom -jar -Xmx512m -Xss256k /maven/app.jar
```
