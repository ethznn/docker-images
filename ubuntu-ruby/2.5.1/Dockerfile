FROM drecom/ubuntu-ruby:2.5.1

LABEL maintainer="prxyeo@gmail.com"

RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    locale-gen en_US en_US.UTF-8 && \
    update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  
ENV LC_ALL en_US.UTF-8  

RUN apt-get update
RUN apt-get install sudo
RUN sudo ln -sf bash /bin/sh
RUN source /etc/default/locale

RUN sudo apt-get install -y postgresql postgresql-contrib postgresql-client
RUN sudo apt-get install -y libpq-dev