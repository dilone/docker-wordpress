# Docker Compose Wordpress (DCW)

A pretty simplified Docker Compose workflow that sets up a containers for local Wordpress development.

## Usage

To get started, make sure you have [Docker installed](https://docs.docker.com/docker-for-windows/install/) on your system, and then clone this repository.

Next, navigate in your terminal to the directory you cloned this, and spin up the containers for the web server by running `docker stack deploy -c stack.yml stack-name`. the project will start on [localhost:8080](http://localhost:8080)

to remove the stack run `docker volume remove stack-name`

After that completes, add a theme to the themes folder and star to build your template.

## Persistent MySQL Storage

By default, the database is persistent, and the data remains after bringing containers down and back up, do the following if you need to delete the volume:

```
docker volume ls
docker volume remove volume-name
```

you can also run `docker volume prune` to remove all volumes from docker.
