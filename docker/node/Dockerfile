FROM node:latest

RUN npm install -g --silent pm2
RUN apt update && apt install sudo

ENV TERM xterm-256color
ENV TZ=Europe/Bucharest
RUN adduser --disabled-password --gecos "" strangehat && \
  echo "strangehat ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN mkdir /app && chown strangehat:strangehat /app

ENV HOST="0.0.0.0"

USER strangehat

CMD ["tail", "-f", "/dev/null"]
# CMD ["/bin/sh", "/app/docker/starter.sh"]
