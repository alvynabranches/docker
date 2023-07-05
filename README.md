# Docker Commands

`docker version` -> Gives the version

`docker info` -> Gives the info

`docker container run --publish 80:80 nginx` -> Runs the Container at port 80 and routes it to port 80 of the host operating system, whose image name is nginx (If the command is runned for the first time then it will download the image and store it on the machine for future use)

`docker container run --publish 80:80 --detach nginx` -> `--detach` or `-d` parameter runs the container in the background

`docker container stop [cid]` -> Stops the running container whose id is specified in the command

`docker container ls` -> Shows all the container that are running

`docker container run --publish 80:80 --detach --name webhost nginx` -> Changes the container name according to what is specified after `--name` parameter

`docker container ls -a` -> Shows all the container that are running as well as stopped once

`docker container logs [cname]` -> Gives the log information of the container whose container name is defined in the command

`docker container top [cname]` -> Gives the list of processes whose container name is defined in the command

`docker container prune` -> Removes all the non-running containers

`docker container run --name mongo -d mongo` -> `-d` parameter is the shortform for `--detach`

`docker container rm [cid]` -> Removes the container (that are stopped) with the specified id. No need to put the full id, first 4-5 characters will work

`docker container rm -f [cid]` -> Removes the container forcefully (even when they are running) with the specified id. No need to put the full id, first 4-5 characters will work

`docker container start [cname]` -> Restarts the stopped container

`docker container inspect [cid/cname]` -> Inspect the container with the specified container id or the container name

`docker container stats` -> Gives the status of all the containers

`docker container stats [cid]` -> Gives the status of the container whose id is specified

`docker container run -it [iname]` -> Run a container with the specified image name

`docker container run -it --name [iname] nginx` -> Run a container with the specifed

`docker container run -it ubuntu` -> Run the container with image name ubuntu

`docker run --publish 80:80 nginx` -> Does the same thing as `docker container run --publish nginx`, but this was used in the older version and hence depricated. Still we can use it because docker is backward compatable

`docker ps` -> Does the same thing as `docker container ls`, but this was used in the older version and hence depricated. Still we can use it because docker is backward compatable

`docker ps -a` -> Does the same thing as `docker container ls -a`, but this was used in the older version and hence depricated. Still we can use it because docker is backward compatable

`docker top [cname]` -> Does the same thing as `docker container top [cname]`, but this was used in the older version and hence depricated. Still we can use it because docker is backward compatable

`docker start [cname]` ->  -> Does the same thing as `docker container start [cname]`, but this was used in the older version and hence depricated. Still we can use it because docker is backward compatable

###### Other Servers
- mysql --> mysql database
- httpd --> apache server

###### Assignments 
1. Run a nginx, mysql, httpd server which should listen on 80:80, 3306:3306, 8080:80 respectively. Run all of them with --detach or -d and name each of them. While running mysql, use the --env or -e option to pass in MYSQL_RANDOM_ROOT_PASSWORD=yes
2. 
