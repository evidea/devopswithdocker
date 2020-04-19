FROM ubuntu
WORKDIR /mydir

ENV API_URL=http://localhost:5000

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y sudo git
RUN sudo apt install -y nodejs
RUN cd /mydir && mkdir frontend-example-docker && git clone https://github.com/docker-hy/frontend-example-docker 
RUN cd /mydir/frontend-example-docker/ && npm install && npm build
CMD cd /mydir/frontend-example-docker/ && npm start

EXPOSE 5000
