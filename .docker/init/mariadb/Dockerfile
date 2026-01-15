FROM mariadb:latest AS mariadb

USER root

RUN groupadd -g 1000 app && \
    useradd -u 1000 -g 1000 -m -s /bin/bash app && \
    usermod -aG app mysql

RUN mkdir -p /var/lib/mysql && \
    chown -R 1000:1000 /var/lib/mysql && \
    chmod -R 777 /var/lib/mysql   # temporário, só para init

USER 1000:1000

WORKDIR /var/lib/mysql
