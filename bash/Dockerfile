# ----------------------------------
# Pterodactyl Core Dockerfile
# Environment: glibc
# Minimum Panel Version: 0.6.0
# ----------------------------------
FROM        node:8-alpine
FROM        python:3-alpine


LABEL       author="RTK" maintainer="rtkhorror23@gmail.com"

RUN         apk add --no-cache --update libc6-compat ffmpeg \
            &&  apk add --no-cache --update \ 
            && adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         ["/bin/ash", "/entrypoint.sh"]
