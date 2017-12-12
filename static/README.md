# Deploying a static container

1) Build the image: `docker build -t surf:v1 .`

2) Run a container using that image: `docker run --name chris-surf -d -p 3000:80 surf:v1`

* note that I calling the running contiainer "chris-surf" but using the image "surf:v1" to create it.

* note that I am also mapping the internal container por 80 to 3000, thus exposing it to the outside on port 3000

3) See it at: `http://localhost:3000`


# Additional commands

* stop container
`docker stop {containerID}`

* helpful command to remove all stopped containers (https://zaiste.net/posts/removing_docker_containers/)
`docker ps -aq --no-trunc | xargs docker rm`

