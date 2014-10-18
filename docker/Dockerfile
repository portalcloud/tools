FROM ubuntu:14.04

RUN apt-get update
# install some components
RUN sudo apt-get update && \
    sudo apt-get install -y git npm && \
    sudo ln -sf /usr/bin/nodejs /usr/bin/node && \
    sudo npm install -g yo generator-angular

RUN mkdir portalcloud
WORKDIR /portalcloud
RUN git clone https://github.com/portalcloud/webapp.git
WORKDIR /portalcloud/webapp
RUN npm install -g grunt
RUN npm install -g grunt-cli
RUN bower search --allow-root
RUN bower install --allow-root
RUN npm install