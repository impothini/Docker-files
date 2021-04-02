FROM ubuntu:16.04
RUN  apt-get update && \
     apt-get -y install wget
RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -

RUN echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list

RUN  apt-get update && \
     apt-get -y install postgresql
USER postgres

RUN    /etc/init.d/postgresql start

