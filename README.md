# Deep Learning Images with docker
This project are combine of essential tools are using in deep learning, machine learning work. We're using **[Keras](https://keras.io/)** on front-framework and [Tensorflow](https://www.tensorflow.org/) on back-framework.

## Requirements
I've been testing on Ubuntu 16.04 with Docker version 17.12.0-ce, build c97c6d6 are build passed. So these are my specification on my testing

 - Ubuntu 16.04 LTS
 - Docker version 17.12.0-ce, build c97c6d6
 - Nvidia driver version 384.111
 - nvidia-docker (essential!)

If you want to run this images, you could have [docker](https://www.docker.com/) engine are installed on your machine.
## How to build this image ?

via docker hub:

> coming soon.

via manual:

    git clone https://github.com/mynameismaxz/docker-deeplearning/
    cd docker-deeplearning
    git checkout master
    docker build -t $USER/docker-deeplearning:latest -f Dockerfile.gpu .
Please wait for building image. After that you can use this image.

## How to run this image ?
We're using nvidia-docker to make container. So you can use this command

    docker run --name docker-deeplearning -v /path/to/your/project/:/workspace/ -p 6006:6006 -p 80:80 -p 8888:8888 -p 3000:3000 mynameismaxz/docker-deeplearning:latest

## Port Usage
|Port| Description  |
|--|--|
| 80 | for cloud9 ide |
| 3000 | for cloud9 ide |
| 6006 | for tensorboard(optional) |
| 8888 | for jupyter |


## Issues & Question

You can submit **issue** and make some question if you have some problem to using this docker images.
