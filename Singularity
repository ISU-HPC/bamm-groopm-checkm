bootstrap:docker
from:continuumio/miniconda

%labels
MAINTAINER Yasasvy Nanyam ynanyam@iastate.edu

%post

export PATH=/opt/conda/bin:$PATH
conda config --add channels conda-forge
conda config --add channels bioconda
conda install bamm
conda install groopm
conda install checkm-genome
