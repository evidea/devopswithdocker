FROM ubuntu
WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
ARG website

CMD echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;
