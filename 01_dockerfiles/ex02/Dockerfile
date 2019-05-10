# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gfielder <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/05/08 12:29:18 by gfielder          #+#    #+#              #
#    Updated: 2019/05/08 17:42:41 by gfielder         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# ----- Prompt ----------------------------------------------------------------
# You are going to create your first Dockerfile to containerize Rails applications
# That’s a special configuration: this particular Dockerfile will be generic,
# and called in another Dockerfile, that will look something like this:
# 
#   FROM ft-rails:on-build
#   EXPOSE 3000
#   CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]
# 
# Your generic container should install, via a ruby container, all the
# necessary dependencies and gems, then copy your rails application in the
# /opt/app folder of your container. Docker has to install the approtiate gems
# when it builds, but also launch the migrations and the db population for your
# application. The child Dockerfile should launch the rails server (see example
# below). If you don’t know what commands to use, it’s high time to look at the
# Ruby on Rails documentation.
# -----------------------------------------------------------------------------

# ----- Notes -----------------------------------------------------------------
# ft-rails:on-build needs to be an existing image first
# Everything starting with ONBUILD in that image's dockerfile  will run right
# after the FROM
# 's' is an alias for 'server', so I substituted it to be clearer
# -b binds an IP address
# -p specifies port
#
# Also fuck this exercise. I'm done.
# -----------------------------------------------------------------------------

FROM ft-rails:on-build
EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0", "-p", "3000"]
