FROM ruby

RUN apt update && apt upgrade

RUN apt install -y build-essential libpq-dev nodejs sqlite3
RUN get install rails -y


ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install && rails db:migrate && rails db:seed
