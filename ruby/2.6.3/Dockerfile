FROM ruby:2.6.3-alpine

RUN apk add --update build-base postgresql-dev tzdata git

RUN apk add --update nodejs yarn

RUN gem install bundle

WORKDIR /app
ADD Gemfile Gemfile.lock /app/

RUN bundle install

EXPOSE 3000
