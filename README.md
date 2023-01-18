# Jax TPU VM Docker Base Image 🚀
![GitHub issues](https://img.shields.io/github/issues/OrenLeung/jax_tpu_docker)
![GitHub contributors](https://img.shields.io/github/contributors/OrenLeung/jax_tpu_docker)
![GitHub last commit](https://img.shields.io/github/last-commit/OrenLeung/jax_tpu_docker)

## About
Provides a Docker image for running JAX on TPU VMs. This repository contains the necessary files to build the Docker image and run JAX on TPUs with ease, making it easy for researchers to take advantage of the power of TPUs for their machine learning projects.

This image is intended to be the base image for JAX on TPU VMs, thus you can extend it via `FROM orenleung:jax_tpu` or directly copying and editing the file itself.

## Run Docker Container
```bash
docker run --net=host --privileged -it --rm orenleung/jax_tpu:latest
```

## Pull Docker Container
```bash
docker pull orenleung/jax_tpu:latest
```

## Build Docker Image
```bash
docker build -t orenleung/jax_tpu .
```

## Anotations
Since `--privileged` is required and `--net=host` is recommended, this docker image to run will require sudo privileges, so make sure that either `docker` daemon is configured to run without sudo or the user is added to `docker` group or the user is root.

## TroubleShoot
if you get this error message
```bash
docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/create": dial unix /var/run/docker.sock: connect: permission denied.
See 'docker run --help'
```
use `sudo` or add your user into the docker group [Docker Post-Install Instructions](https://docs.docker.com/engine/install/linux-postinstall/)


## References
- [https://github.com/tensorflow/tpu/blob/master/tools/docker/Dockerfile](https://github.com/tensorflow/tpu/blob/master/tools/docker/Dockerfile)
