FROM ubuntu
MAINTAINER Laurent Perrin

RUN apt-get update && apt-get install -y mariadb-client cron

COPY ./backup-db /etc/cron.d/backup-db

RUN chmod 0644 /etc/cron.d/backup-db

RUN touch /var/log/cron.log

CMD cron && tail -f /var/log/cron.log
