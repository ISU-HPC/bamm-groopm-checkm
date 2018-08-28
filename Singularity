bootstrap:docker
from:continuumio/miniconda

%labels
MAINTAINER Yasasvy Nanyam ynanyam@iastate.edu

%post
apt update
apt install -y gcc libgl1-mesa-glx
export PATH=/opt/conda/bin:$PATH
conda config --add channels conda-forge
conda config --add channels bioconda
conda install bamm 
pip install --no-cache-dir cython GroopM pillow refinem 
ln -s /opt/conda/lib/libhts.so /opt/conda/lib/libhts.so.1
conda install checkm-genome
conda install functools_lru_cache
echo 'export PATH=/usr/local/bin:/opt/conda/bin:$PATH' >>$SINGULARITY_ENVIRONMENT
rm -rf /var/lib/apt/lists/*
# INSTALL PRODIGAL
apt install -y build-essential
cd /opt
git clone https://github.com/hyattpd/Prodigal.git
cd Prodigal
make install
cd ..
rm -rf Prodigal
#INSTALL BLAST+
apt install -y ncbi-blast+
# INSTALL DIAMOND
cd /opt
wget http://github.com/bbuchfink/diamond/releases/download/v0.9.22/diamond-linux64.tar.gz
tar xzf diamond-linux64.tar.gz
cd diamond-linux64
cp diamond /usr/local/bin
cd ..
rm -rf diamond-linux64*
