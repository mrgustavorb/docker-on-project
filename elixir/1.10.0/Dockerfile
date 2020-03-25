FROM elixir:1.10-alpine

WORKDIR /app

RUN apk update && \
    apk add --update build-base \
    postgresql-dev \
    tzdata \
    inotify-tools \
    musl \
    musl-dev \
    musl-utils \
    nodejs \
    yarn

RUN mix local.hex --force
RUN mix local.rebar --force

RUN mix archive.install --force hex phx_new 1.4.16

EXPOSE 4000
