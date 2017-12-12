# Deploying a static container

### Build the image
```
docker build -t surf:v1 .
```

### Run container 

```
docker run --name chris-surf -d -p 3000:80 surf:v1

* note that I am calling the running container "chris-surf" but using the image "surf:v1" to create it

* note that I am also mapping the internal container por 80 to 3000, thus exposing it to the outside on port 3000
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

