# A container for Illumina basemount
https://basemount.basespace.illumina.com/  

This repo is a fork from https://github.com/muccg/docker-basemount  
I had to modify the Dockerfile and bash script and am providing additional information for using the container. 

## Running Basemount using Docker on a Mac  
Before setting up the container will need to have docker running first.  I used Kitematic (https://kitematic.com/) and started the Docker command-line using the Kitematic GUI interface.  

### Code to install and run the container  
```
# clone repo
git clone https://github.com/nate-d-olson/docker-basemount` 
  
# build container 
docker build -t basemount docker-basemount/.

# Creating directory on host system for mounting Basespace `
mkdir BaseSpace  
* Running the basemount container 
bash docker-basemount/basemount BaseSpace/   
# From within the container 
basemount BaseSpace/

```

When basemount starts up you will need to authorize access to basespace, basemount provides a URL to use for authorizing access.  See Basemount documentation for additional information about authorization, ect.  

### Transfering files
After the container is up and running use `cp` or `rsync` to transfer files to local system.  The download speed was slow for me, I not sure if it is my system or using basemount with Docker.   

