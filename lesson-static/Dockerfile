FROM nginx:alpine
COPY . /usr/share/nginx/html

# Greet our executives
#CMD ["echo","Hello World! Wish I was surfing."]




### BUILD
# docker build -t chris-surf:v8 .

### RUN
# docker run --name chris-surf-v8 -d -p 3000:80 chris-surf:v8


### remove all stopped containers (https://zaiste.net/posts/removing_docker_containers/)
# docker ps -aq --no-trunc | xargs docker rm