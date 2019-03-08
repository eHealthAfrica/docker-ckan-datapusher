# Datapusher CKAN image  ![Docker Pulls](https://img.shields.io/docker/pulls/keitaro/ckan-datapusher.svg)

## Overview

This repository contains base docker image used to build [CKAN Datapusher](https://docs.ckan.org/projects/datapusher/en/latest/). It's based on [Alpine Linux](https://alpinelinux.org/).

## Build

To create new image run:

```sh 
docker build --tag ckan-datapusher . 
``` 
The –-tag ckan-datapusher flag sets the image name to ckan-datapusher and the dot ( “.” ) at the end tells docker build to look into the current directory for Dockerfile and related contents.

## List

Check if the image shows up in the list of images:
```sh
 docker images
```

## Run

To start and test newly created image run:
```sh
 docker run ckan-datapusher
```
By default DataPusher should be running at the following port:

>http://localhost:8800/

## Upload to DockerHub

>*It's recommended to upload built images to DockerHub* 

To upload the image to DockerHub run:

```sh 
docker push [options] <docker-hub>/ckan:<datapusher-tag> 
```

## Upgrade 

To upgrade the Docker file to use new CKAN datapusher version, in the Dockerfile you should change:

>ENV GIT_BRANCH={datapusher_release} 

Check [CKAN datapusher repository](https://github.com/ckan/datapusher/releases) for the latest releases. 

## Configuring the maximum upload size 

To change this value you can specify the MAX_CONTENT_LENGTH setting in datapusher_settings.py.

