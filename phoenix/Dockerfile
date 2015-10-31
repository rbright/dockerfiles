FROM rbright/elixir:latest
MAINTAINER Ryan Bright <ryan@rbright.net>

# Set the Phoenix version
ENV PHOENIX_VERSION 1.0.3

# Install Phoenix and dependencies
RUN mix archive.install https://github.com/phoenixframework/phoenix/releases/download/v$PHOENIX_VERSION/phoenix_new-$PHOENIX_VERSION.ez --force
