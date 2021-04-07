# Docker-files

Docker image modification Task

Added the following lines in Dockerfile under #bedtools
RUN cd /opt && \
	wget https://github.com/arq5x/bedtools2/releases/download/v2.27.1/bedtools-2.27.1.tar.gz && \
        tar -xf bedtools-2.27.1.tar.gz && rm bedtools-2.27.1.tar.gz && \
        cd /opt/bedtools2 && make
ENV PATH /opt/bedtools2/bin:$PATH

After modifying the Dockerfile, change directory to folder where the Dockerfile is present 
cd /c/Users/savit/Documents/WU_Tasks/Task12-docker

Build command for the task is: 
docker build .

Viewing the image files
docker image ls

Running the interactive docker container by providing the image ID
docker run -i -t <IMAGE_ID> /bin/bash

which bedtools (now shows that bedtools is installed)
/opt/bedtools2/bin/bedtools

