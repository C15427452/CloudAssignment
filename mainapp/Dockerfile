FROM ubuntu:latest
MAINTAINER C15427452
RUN apt-get update
RUN apt-get -y upgrade
ADD /mainapp /mainapp
RUN pip install -r /mainapp/requirements.txt
EXPOSE 8080
WORKDIR /mainapp
RUN mkdir /lala
CMD python mainapp.py
