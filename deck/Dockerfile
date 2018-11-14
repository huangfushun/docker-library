FROM node:8.9.0
MAINTAINER Kamil Karczmarczyk <kkarczmarczyk@gmail.com> # Global install yarn package manager 
RUN apt-get update && apt-get install -y unzip curl apt-transport-https && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y yarn
RUN cd /opt && \
     wget https://github.com/spinnaker/deck/archive/version-2.5.4.zip && \
     unzip -q version-2.5.4.zip && \
     mv deck-version-2.5.4 deck && \
     cd deck && \
     yarn
WORKDIR /opt/deck
