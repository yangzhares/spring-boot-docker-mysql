FROM java:8

WORKDIR /app
COPY demo.jar /app/demo.jar
RUN useradd -ms /bin/bash admin && chown admin:admin demo.jar && bash -c 'touch demo.jar'
USER admin
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","demo.jar"]
