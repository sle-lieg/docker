FROM ruby:2.4

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y nodejs \
&& gem install rails

ONBUILD WORKDIR /opt/app
ONBUILD COPY . /opt/app
ONBUILD RUN bundle install && rake db:migrate && rake db:seed
