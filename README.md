# doo

```
> doo help

Usage: doo COMMAND [arg...]

A docker assistant to build, ship and run containers.

The image NAME is built using the name of the current directory and the env var DOCKER_REPO.
and is required to build, tag and push`.

dev and go run containers by using all *.env files found in the current
directy in --env-file arguments and all directories that appears in COPY directives
with --volume.

Commands:
  b, build      docker build $DOCKER_REPO/$NAME
  t, tag        docker tag   $DOCKER_REPO/$NAME:VERSION (latest and sha1 of current directory if git)
  p, push       docker push  $DOCKER_REPO/$NAME

  u, up         docker compose up -d using the first .yml found in the current directory
  c ARGS...     docker compose ARGS  using the first .yml found in the current directory

  d, dev        docker run $DOCKER_REPO/$NAME with env-files and local directories as volumes
  g, go  IMAGE  docker run $IMAGE with env-files and local directories as volumes
```

