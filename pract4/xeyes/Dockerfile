FROM ubuntu:latest

RUN apt-get update && apt-get install -y x11-apps xauth && rm -r /var/lib/apt/lists/*
ENV DISPLAY=host.docker.internal:0
CMD ["xeyes"]