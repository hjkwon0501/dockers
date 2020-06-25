# dockerfiles-ubuntu-user-adderable
Ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t hjkwon0501/ubuntu .
	docker run -it --name u1 -e USER=hjkwon0501 -e PASSWD=hjkwon0501 hjkwon0501/ubuntu
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        hjkwon0501/ubuntu      "/bin/bash"         7 seconds ago       Up 6 seconds                            u1
```

To test, ("nowage" is username. )
```
	su - nowage
```
To Rollback
```
    docker rm u1 -f
    docker rmi hjkwon0501/ubuntu
```
