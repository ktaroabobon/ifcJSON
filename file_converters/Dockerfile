FROM continuumio/miniconda3

ENV APP_PATH=/code \
    PYTHONPATH=.
#　開発物のソースコードはcodeデイレクトリ下に配置する

RUN conda create -n ifc2json python==3.8

SHELL ["conda", "run", "-n", "ifc2json", "/bin/bash", "-c"]
RUN conda install -c conda-forge -c oce -c dlr-sc -c ifcopenshell ifcopenshell
RUN conda install -c conda-forge poetry
RUN conda install -c conda-forge poetry-core

WORKDIR $APP_PATH

RUN apt-get update && \
    apt-get upgrade -y

EXPOSE 8000