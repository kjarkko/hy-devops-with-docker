FROM openjdk:buster

WORKDIR /src/
COPY . . 
RUN ./mvnw package

WORKDIR /app/
RUN mv /src/target/docker-example-1.1.3.jar ./application.jar && \
    rm -rf /src/ /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /app/
USER app 

CMD ["java", "-jar", "./application.jar"]
