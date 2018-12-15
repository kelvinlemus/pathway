# Docker

## Commands
- `docker ps`, list runnning containers
  + `-a`, show all containers
  + `-q`, only display numeric id's
- `docker inspect NAME|ID`, return low-level information
  + `-f {{ json.Config.Env }}`
    + Example: `docker inspect -f '{{ json .Config.Env  }}' c5884d6b1e43`
- `docker rename CONTAINER NEW_NAME`
  + Example: `docker rename c5884d6b1e43 hola_mundo`
- `docker rm`
  + Example: `docker rm $(docker ps -aq)`

## Links
- https://itnext.io/chroot-cgroups-and-namespaces-an-overview-37124d995e3d
