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