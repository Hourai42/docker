FROM ruby

RUN apt-get update -y && apt-get upgrade -y && \
        gem install rails && \
        apt-get install nodejs -y && \
        apt-get autoclean -y && apt-get clean -y

ONBUILD COPY app/ /opt/app
WORKDIR /opt/app

ONBUILD RUN bundle install && \
                rails db:migrate && \
                rails db:setup && \
                rails db:seed
