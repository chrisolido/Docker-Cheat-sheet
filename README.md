# Docker-Cheat-sheet

Container run
docker create creates a container but does not start it.
docker rename allows the container to be renamed.
docker run creates and starts a container in one operation.
$ docker run -it ubuntu-ssh-k /bin/bash
i: interactive, t: with tty
docker rm deletes a container.
docker update updates a container's resource limits.


Container info
docker ps shows running containers.
$ docker ps 
CONTAINER ID        IMAGE                 COMMAND             CREATED             STATUS              PORTS               NAMES
e2481c1bad5d        ubuntu-ssh-k:latest   "/bin/bash"         10 hours ago        Up 10 hours                             hopeful_carson 
docker logs gets logs from container. (You can use a custom log driver, but logs is only available for json-file and journald in 1.10)
docker inspect looks at all the info on a container (including IP address).
To get an IP address of a running container:
$ docker inspect --format '{{ .NetworkSettings.IPAddress }}' $(docker ps -q)
172.17.0.5
docker events gets events from container.
docker port shows public facing port of container.
docker top shows running processes in container.
docker stats shows containers' resource usage statistics.
docker diff shows changed files in the container's FS.
