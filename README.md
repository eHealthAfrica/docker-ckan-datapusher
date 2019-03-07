# Base docker ckan datapusher image 

## Overview

This repository contains base docker image used to build datapusher instance images. 

## Build
To create the image 

```sh 
docker build -t datapusher-0.0.14 . 
``` 

## Upload to DockerHub

>*It's recommended to upload built images to DockerHub* 

To upload the image to DockerHub

```sh 
docker push [options] ehealthafrica/datapusher:<image-tag> 
