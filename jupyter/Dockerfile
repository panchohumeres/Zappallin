FROM jupyter/base-notebook

USER root

RUN apt-get update
RUN apt-get -qq -y install curl
RUN apt-get install cron -yqq
RUN apt-get install -y rar unrar
#RUN apt-get install --assume-yes postfix


RUN python --version

USER $NB_UID

RUN conda install --quiet --yes -c \
    pandas \
    matplotlib
    #pyspark=3.0  \ 
    #openjdk=8


VOLUME /home/jovyan/work
WORKDIR /home/jovyan/work
