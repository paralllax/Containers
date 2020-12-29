FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN sudo apt-get update && \
	sudo apt-get upgrade -y && \
	sudo apt-get install ca-certificates apt-transport-https wget -y && \
	echo 'deb https://www.ui.com/downloads/unifi/debian stable ubiquiti' \
		| sudo tee /etc/apt/sources.list.d/100-ubnt-unifi.list && \
	sudo wget -O /etc/apt/trusted.gpg.d/unifi-repo.gpg https://dl.ui.com/unifi/unifi-repo.gpg && \
	sudo apt-mark hold openjdk-11-* && \
	sudo apt-get update && \
	sudo apt-get install unifi -y && \

