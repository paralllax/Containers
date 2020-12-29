FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Chicago

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install apache2 apache2-utils -y && \
	apt-get clean

EXPOSE 80

ENTRYPOINT ["apache2ctl", "-D", "FOREGROUND"]
