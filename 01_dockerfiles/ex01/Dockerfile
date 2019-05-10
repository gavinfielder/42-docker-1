# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gfielder <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/05/08 12:29:18 by gfielder          #+#    #+#              #
#    Updated: 2019/05/08 14:35:17 by gfielder         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# ----- Prompt ----------------------------------------------------------------
# From a debian image you will add the appropriate sources to create a
# Teamspeak server, that will launch along with your container. It will be
# deemed valid if at least one user can connect to it and engage in a normal
# discussion (no far-fetched setup), so be sure to create your Dockerfile with
# the sources when it builds, they cannot be in your repository.
# -----------------------------------------------------------------------------

# ----- Notes -----------------------------------------------------------------
# https://forum.teamspeak.com/threads/132611-Install-teamspeak-3-server-on-Debian-8
# https://hub.docker.com/_/teamspeak
# 
# Based on the docker documentation, EXPOSE doesn't do anything relevant
# to this use, but may do some things related to inter-container communication.
# The user needs to use docker run with either expose or publish in order to
# make the ports actually available when running the app
# 
# ENV specifies environment variables to set inside the image
# WORKDIR (obviously?) sets the current working directory
# -----------------------------------------------------------------------------

FROM debian
ENV TS3SERVER_LICENSE=accept
WORKDIR /home/teamspeak
EXPOSE 9987/udp 10011 30033
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget bzip2
RUN wget http://dl.4players.de/ts/releases/3.7.1/teamspeak3-server_linux_amd64-3.7.1.tar.bz2
RUN tar -xvf teamspeak3-server_linux_amd64-3.7.1.tar.bz2

WORKDIR teamspeak3-server_linux_amd64
ENTRYPOINT sh ts3server_minimal_runscript.sh
