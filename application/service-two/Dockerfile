FROM openjdk:8-jre
# environment
EXPOSE 8084
# executable ADD @project.artifactId@-@project.version@.jar app.jar
ADD target/service-two.jar app.jar
# run app as user 'booter'
RUN /bin/sh -c 'touch /app.jar'
ENTRYPOINT ["java", "-Xmx256m", "-Xss32m", "-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
