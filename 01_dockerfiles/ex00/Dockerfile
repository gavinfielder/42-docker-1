# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gfielder <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/05/08 12:29:18 by gfielder          #+#    #+#              #
#    Updated: 2019/05/08 12:42:17 by gfielder         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# ----- Prompt ----------------------------------------------------------------
# From an alpine image you’ll add to your container your favorite text editor,
# vim or emacs, that will launch along with your container.
# -----------------------------------------------------------------------------

# ----- Notes -----------------------------------------------------------------
# FROM specifies the base image. Dockerfiles must start with this or ARG
# RUN runs commands inside the image.
# ENTRYPOINT specifies the command that's run automatically
# 
# `docker build -t image-name .` runs this Dockerfile, creating a new image
# using the current directory as the build context
# Once the image is built, `docker run --rm -it image-name` makes a container,
# runs the container interactively, and deletes the container on exit
# -----------------------------------------------------------------------------

FROM alpine

RUN apk update && apk upgrade
RUN apk add vim

ENTRYPOINT vim
