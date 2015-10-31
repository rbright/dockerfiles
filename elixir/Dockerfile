FROM buildpack-deps:trusty-curl
MAINTAINER Ryan Bright <ryan@rbright.net>

# Enable UTF-8 encoding
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# Install Erlang
RUN wget http://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb \
  && dpkg -i erlang-solutions_1.0_all.deb \
  && apt-get update \
  && apt-get install -y erlang erlang-ssl erlang-inets \
  && rm erlang-solutions_1.0_all.deb

# Install Elixir
RUN apt-get install elixir

# Install Hex package manager
RUN mix local.hex --force && mix local.rebar --force

# Run Elixir's interactive shell
CMD ["iex"]
