bootstrap:docker
from:continuumio/miniconda

%labels
MAINTAINER Yasasvy Nanyam ynanyam@iastate.edu

%post
apt install -y gcc libgl1-mesa-glx
export PATH=/opt/conda/bin:$PATH
conda config --add channels conda-forge
conda config --add channels bioconda
conda install bamm
pip install --no-cache-dir cython GroopM pillow refinem funtools
ln -s /opt/conda/lib/libhts.so /opt/conda/lib/libhts.so.1
conda install checkm-genome
echo 'export PATH=/opt/conda/bin:$PATH' >>$SINGULARITY_ENVIRONMENT
rm -rf /var/lib/apt/lists/*
