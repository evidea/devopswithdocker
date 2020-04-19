FROM ubuntu
WORKDIR /mydir

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y sudo git
RUN sudo apt install -y nodejs
RUN cd /mydir && mkdir backend-example-docker && git clone https://github.com/docker-hy/backend-example-docker
RUN cd /mydir/backend-example-docker/ && npm install
CMD cd /mydir/backend-example-docker/ && npm start

EXPOSE 8000
