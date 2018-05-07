FROM nginx:alpine
COPY default.conf /etc/nginx/conf.d/default.conf
COPY . /usr/share/nginx/html


#COPY index.html /usr/share/nginx/html/index.html
#COPY kellyswave.gif /usr/share/nginx/html/kellyswave.gif

# Greet our executives
CMD ["echo","Hello World! Wish I was surfing."]

### BUILD
# docker build -t chris-surf:v8 .

### RUN
# docker run --name chris-surf-v8 -d -p 3000:80 chris-surf:v8


### remove all stopped containers (https://zaiste.net/posts/removing_docker_containers/)
# docker ps -aq --no-trunc | xargs docker rm

