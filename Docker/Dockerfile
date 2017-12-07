#This docker file will create a docker container for the CommonKmers method
#docker run --rm -t -i cami/profiling

FROM cami/profiling

MAINTAINER David Koslicki version: 0.1

#Install required packages
RUN apt-get -y update && \
 apt-get install -y wget && \
 apt-get install -y g++ && \
 apt-get install -y build-essential && \
 apt-get install -y git && \
 apt-get install -y gzip
 
#Install python
RUN apt-get -y update && \ 
 apt-get install -y python3.5 && \
 apt-get install -y python3.5-dev python3.5-venv make libc6-dev g++ zlib1g-dev python3-pip

 
#Install Soumash
RUN pip install -U pip && \
 pip install -U Cython && \
 pip install -U jupyter jupyter_client ipython pandas matplotlib scipy scikit-learn khmer && \
 pip install -U https://github.com/dib-lab/sourmash/archive/master.zip


#Get wrapper/format conversion code
RUN git clone https://github.com/dkoslicki/CAMISourmash.git && \
# cp /CAMIKraken/Docker/default /dckr/etc/tasks.d/default && \
# cp /CAMIKraken/Docker/train /dckr/etc/tasks.d/train && \
# cp /CAMIKraken/src/KrakenToCAMI.py /usr/local/sbin/ && \
# cp /CAMIKraken/src/generate_taxonomy_taxid.py /usr/local/sbin/

