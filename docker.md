# Docker

## Commands
- `docker login`
- `docker ps`, list runnning containers
  + `-a`, show all containers
  + `-q`, only display numeric id's
- `docker inspect NAME|ID`, return low-level information
  + `-f {{ json.Config.Env }}`
    + Example: `docker inspect -f '{{ json .Config.Env  }}' c5884d6b1e43`
- `docker rename CONTAINER NEW_NAME`
  + Example: `docker rename c5884d6b1e43 hola_mundo`
- `docker rm`
  + `-f`
  + Example: `docker rm $(docker ps -aq)`
- `docker run IMAGE`
  + `-rm`, automatically remove the container when it exits
  + `-d`, run container un background
  + `-it`, run interactive shell
  + `--mount src=dbdata,dst=/data/db`, attach a filesystem mount to the container
- `docker exec CONTAINER`, run a command in a running container
  + `-it`, run interactive shell
    + Example: `docker exec -it zealous_lamport bash`
- `docker volume`
  + `docker volume ls`
  + `docker volume prune`
  + `docker volume create dbdata`
  + Example: `docker run -d --name db --mount src=dbdata,dst=/data/db mongo`
- `docker image`
  + `docker image ls`
- `docker tag`
  + `docker tag ubuntu:kelvintest kelvinlemus/ubuntu:kelvintest`
- `docker build`
  + `docker build -t ubuntu:kelvintest .`
- `docker history`
  + `docker history ubuntu:kelvintest`

## Links
- https://itnext.io/chroot-cgroups-and-namespaces-an-overview-37124d995e3d
- https://docs.docker.com/storage/
- https://github.com/wagoodman/dive

