#FROM dtr-uscm.ddc2.prod-shared.aws.lmig.com/jenkinsuser/alpine
FROM node:7-alpine

RUN mkdir -p /src/app

WORKDIR /src/app

COPY package.json /src/app/package.json
COPY .npmrc /src/app/.npmrc

RUN node --version
RUN npm --version

RUN npm install

COPY . /src/app

EXPOSE 3000

CMD [ "npm", "start" ]


### BUILD
# docker build -t chris-node:v2 .

# docker run -d --name chris-node -p 3001:3000 chris-node:v2