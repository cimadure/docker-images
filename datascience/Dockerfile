FROM continuumio/anaconda3

MAINTAINER Ronan Cimadure <ronan.cimadure@gmail.com>

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

RUN mkdir /datascience
WORKDIR /datascience
ADD requirements.txt /datascience/
RUN pip install -r requirements.txt

#RUN conda config --add channels conda-forge
#RUN conda install orange3

# Install apt packages
RUN apt-get update && apt-get install -y \
    freetds-bin \
    freetds-common \
    freetds-dev


RUN export PYMSSQL_BUILD_WITH_BUNDLED_FREETDS=1
RUN pip install pymssql
RUN pip install psycopg2
