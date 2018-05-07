# Deploying a static container

### Build the image
```
docker build -t surf:v1 .
```

### Run container 

```
docker run --name chris-surf-v1 -it -p 3000:80 surf:v1 nginx -g 'daemon off;'


docker run --name chris-surf-v3 -it -p 3000:80 surf:v3 nginx -g 'daemon off;'


* note that I am calling the running container "chris-surf" but using the image "surf:v1" to create it

* note that I am also mapping the internal container por 80 to 3000, thus exposing it to the outside on port 3000

* note I had to add nginx -g 'daemon off;' to get nginx started in foregroud so the container didnt exit (https://www.techietown.info/2016/12/run-nginx-docker/)
```



### See it running 
```
docker ps //you should see your container running

http://localhost:3000
```


### Additional commands

stop container
```
docker stop {containerID}
```

helpful command to remove all stopped containers (https://zaiste.net/posts/removing_docker_containers/)
```
docker ps -aq --no-trunc | xargs docker rm
```

remove single container
```
docker rm {containerID}
```

list all containers
```
docker container ls --all
```

list running containers only
```
docker ps -a
```


