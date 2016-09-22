# doo

```
> doo help
Usage: doo COMMAND [arg...]

A docker assistant to build, ship and run containers.

The image NAME is built using the name of the current directory and the env var DOCKER_REPO.
and is required to build, tag and push`.

dev and go run containers by using all *.env files found in the current directy in --env-file
arguments and all directories that appears in the COPY Dockerfile directives with --volume.

Commands:
  b, build        docker build $DOCKER_REPO/$NAME
  t, tag          docker tag   $DOCKER_REPO/$NAME:VERSION (VERSION: sha1 if git repo and/or latest)
  p, push         docker push  $DOCKER_REPO/$NAME

  u, up                        docker compose up -d by using the first .yml found in the current directory
  dc [COMPOSE_FILE] ARGS...    docker compose ARGS  by using the first .yml found in the current directory or
                               a given compose file

  d, dev          docker run -ti $DOCKER_REPO/$NAME by loading env-files and mounting current directories
  g, go  IMAGE    docker run $IMAGE                 by loading env-files and mounting current directories
```

