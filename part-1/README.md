# Part 1.1

## Exercise 1.1: Getting started
``` 
ville@RB18:~$ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                          PORTS     NAMES
caf3335d4e64   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute               80/tcp    condescending_lederberg
ec4ea56d4d51   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 14 seconds ago                 adoring_pare
0bc8dff0ae2f   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 8 seconds ago                  strange_cori 
```
## Exercise 1.2: Cleanup
````
ville@RB18:~$ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS     NAMES
caf3335d4e64   nginx     "/docker-entrypoint.…"   5 minutes ago   Up 5 minutes   80/tcp    condescending_lederberg

ville@RB18:~$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED      SIZE
nginx        latest    9eee96112def   3 days ago   142MB
````

# Part 1.2
## Exercise 1.3: Secret message
```
ville@RB18:~$ docker run -d --name secret devopsdockeruh/simple-web-service:ubuntu
042640bb44dce5e606eab87d1d7968f52094fe67eb17197562882a56678dec01

ville@RB18:~$ docker exec -it secret bash
root@042640bb44dc:/usr/src/app# tail -f ./text.log
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```

## Exercise 1.4: Missing dependencies
Command used to start the process:
```
ville@RB18:~$ docker run -it ubuntu sh -c 'apt-get update; apt-get install -y curl; echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```

# Part 1.3
## Exercise 1.5: Sizes of images
```
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   23 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   23 months ago   15.7MB
```

## Exercise 1.6: Hello Docker Hub
```
ville@RB18:~$ docker run -it devopsdockeruh/pull_exercise

You found the correct password. Secret message is:
"This is the secret message"
```