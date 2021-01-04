FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Chicago

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install wget openjdk-8-jre -y && \
	apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
	wget "https://launcher.mojang.com/v1/objects/35139deedbd5182953cf1caa23835da59ca3d7cd/server.jar" -P /usr/local/games 

RUN echo "eula=true" > eula.txt

EXPOSE 25565

ENTRYPOINT ["java", "-Xmx1024M", "-Xms1024M", "-jar", "/usr/local/games/server.jar", "nogui"]
