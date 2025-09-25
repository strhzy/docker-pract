FROM ubuntu:latest

WORKDIR /app
COPY calc.jar .

RUN apt-get update && apt-get install -y x11-apps xauth openjdk-17-jre && rm -r /var/lib/apt/lists/*
ENV DISPLAY=host.docker.internal:0
CMD ["java", "-jar", "/app/calc.jar"]