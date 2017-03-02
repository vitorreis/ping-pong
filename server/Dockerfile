FROM ruby:2.4.0
MAINTAINER vitor.reis7@gmail.com
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /ping-pong-service

WORKDIR /ping-pong-service

ADD Gemfile /ping-pong-service/Gemfile
ADD Gemfile.lock /ping-pong-service/Gemfile.lock

RUN bundle install

ADD . /ping-pong-service
