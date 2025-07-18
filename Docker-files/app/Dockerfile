# Stage 1: Building the Application Artifact
FROM openjdk:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone ("put in your repository link")
RUN cd ("put in your repository name") && git checkout docker && mvn install

# Stage 2: Creating the Final Application Image
FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
