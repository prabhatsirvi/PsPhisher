# Dockerfile

# Author       : Prabhat Solanki
# Github       : https://github.com/Prabhatsolanki00
# Email        : prabhatsirvi@gmail.com
# Date         : 10-08-2024
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/Prabhatsolanki00/PsPhisher"

# Working directory
WORKDIR /PsPhisher/
# Add files 
ADD . /PsPhisher

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install python3-pip php openssh-client -y
RUN pip3 install -r files/requirements.txt --break-system-packages
RUN apt-get clean

# Main command
CMD ["python3", "PsPhisher.py", "--noupdate"]

## Wanna run it on your own? Try the following commands:

## "sudo docker build . -t prabhatsolanki00/PsPhisher:latest", "sudo docker run --rm -it prabhatsolanki00/PsPhisher:latest"

## "sudo docker pull prabhatsolanki00/PsPhisher", "sudo docker run --rm -it prabhatsolanki00/PsPhisher"
