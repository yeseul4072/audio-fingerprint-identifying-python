# Truthy
FROM ubuntu:14.04 

# Install dependency packages
RUN apt-get update \
    && apt-get install -y git wget vim libav-tools \
    && apt-get install -y python python-pip \
    && apt-get install -y python-numpy python-matplotlib python-termcolor python-scipy python-pyaudio

# Working directory
RUN mkdir /app
WORKDIR /app

# Install pydub with source codes manually
COPY pydub-0.25.1.tar.gz /app
RUN tar xf pydub-0.25.1.tar.gz
WORKDIR /app/pydub-0.25.1
RUN python setup.py install

# Let start
WORKDIR /app/
