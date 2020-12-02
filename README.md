FFMUC Image Build Docker
========================

I use a Docker container based on this Dockerfile to locally hack on the Freifunk München firmware ( https://github.com/freifunkMUC/site-ffm/ ).

## Warning ⚠️
This is not suitable to build widely used images for a whole bunch of reasons. It is intended for local development only.

## Usage
* Build image
  ```shell
  docker build . -t ffmuc-image-build-docker:v0.0.1
  ```
* Clone `site-ffm` repository to your working directory
  ```shell
  git clone https://github.com/freifunkMUC/site-ffm.git site-ffm
  ```
* Run Docker container mounting your `site-ffm` clone to `/site-ffm` inside the container
  ```shell
  docker run --rm -it -v $(pwd)/site-ffm:/site-ffm ffmuc-image-build-docker:v0.0.1 /bin/bash
  ```
