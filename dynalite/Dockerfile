FROM ubuntu:14.04.3
MAINTAINER Ryan Bright <ryan@rbright.net>

# Install LevelDB and Node.js
RUN apt-get -y update \
  && apt-get -y install libleveldb-dev libleveldb1 nodejs-legacy npm

# Clean the package cache
RUN apt-get -y clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Install Dynalite
RUN npm install -g dynalite

# Expose a port for the Dynalite server
ENV PORT 4567
EXPOSE $PORT

# Start the Dynalite server
CMD dynalite --port $PORT
