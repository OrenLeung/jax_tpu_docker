# Jax TPU VM Docker 

## Run Docker Container
```bash
docker run --net=host --privileged -it --rm orenleung/jax_tpu:latest
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
