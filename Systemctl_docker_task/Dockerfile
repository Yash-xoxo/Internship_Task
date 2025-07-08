FROM ubuntu:20.04

RUN apt update && apt install -y apache2 supervisor

# Create a Supervisor config file
RUN mkdir -p /var/log/supervisor
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 80
CMD ["/usr/bin/supervisord"]
