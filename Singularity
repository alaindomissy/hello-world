Bootstrap: docker
From: ubuntu:14.04

%post

wget --quiet https://repo.continuum.io/miniconda/Miniconda2-4.3.14-Linux-x86_64.sh -O ~/miniconda.sh
/bin/bash ~/miniconda.sh -b -p /opt/conda
rm ~/miniconda.sh

# doing this here as the environment section is not processed yet  
# is this going to be ok ^^^^^^^^^^^^
PATH=/opt/conda/bin:$PATH

# just because I was too lazy to type the full absolute path for /opt/conda/bin/conda
conda install -c auto pypihello 

%labels
MAINTAINER vanessasaur
WHATAMI dinosaur

%environment
DINOSAUR=vanessasaurus
export DINOSAUR

%files
rawr.sh /rawr.sh

%runscript
exec /bin/bash /rawr.sh
