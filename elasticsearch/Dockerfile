FROM ubuntu
MAINTAINER J. Scott Miller j.scott.miller@gmail.com

# Update the base image
RUN apt-get update
RUN apt-get upgrade

# Install wget so we can grab docker
RUN apt-get install -y wget

# Grab the docker deb and install it
RUN wget --no-check-certificate https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.5.deb
RUN dpkg -i elasticsearch-0.90.5.deb

# Our entry point will be elasticsearch, running in the foreground by default
ENTRYPOINT ["elasticsearch"]
CMD ["-f"]

# We'll want to expose port 9200 for API access
EXPOSE 9200 
