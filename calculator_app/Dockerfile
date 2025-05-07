FROM maven AS build
WORKDIR /app
COPY ./app
RUN mvn clean package

FROM tomcat
COPY --from=build /app/target/calculator.war /usr/local/tomcat/webapps/calculator.war