#############################################################################

# Dockerfile to build bowtie2 
# Based on Debian Stretch

#############################################################################

FROM ubuntu:16.04

LABEL maintainer="Pedro Cerqueira, pedro.cerqueira@medicina.ulisboa.pt"

RUN apt-get update && apt-get install -y \
    unzip \
    wget \
    libsys-hostname-long-perl \
    python \
    gcc \
    g++ \
    libtbb-dev


WORKDIR /NGStools/
ENV work_dir="/NGStools/bowtie2-2.3.2"

# Bowtie v2.3.2
RUN wget https://downloads.sourceforge.net/project/bowtie-bio/bowtie2/2.3.2/bowtie2-2.3.2-linux-x86_64.zip
RUN unzip bowtie2-2.3.2-linux-x86_64.zip
RUN rm -rf bowtie2-2.3.2-linux-x86_64.zip


#ADD BOWTIE TO PATH
ENV PATH="${work_dir}:${PATH}"

RUN bowtie2 --help


    
