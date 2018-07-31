bootstrap:docker
from:continuumio/miniconda

%labels
MAINTAINER Yasasvy Nanyam ynanyam@iastate.edu

%post
apt install -y gcc
export PATH=/opt/conda/bin:$PATH
conda config --add channels conda-forge
conda config --add channels bioconda
conda install bamm
pip install --no-cache-dir cython GroopM
conda install checkm-genome
