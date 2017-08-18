FROM continuumio/anaconda

MAINTAINER Ronan Cimadure <ronan.cimadure@gmail.com>

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

RUN pip install -r requierements.txt

#RUN conda config --add channels conda-forge
#RUN conda install orange3

# Install apt packages
RUN apt-get update && apt-get install -y \
    freetds-bin \
    freetds-common \
    freetds-dev

#psycopg2
#pymssql
