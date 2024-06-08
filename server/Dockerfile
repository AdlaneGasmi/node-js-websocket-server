# create docker image that we will start as coountainer
# we need to build the docker image
# docker build -t or --tag image name:<image tag> <location of docker file> (. for current directory)
FROM node:22-alpine
#COPY <src> on our machine <dest> in tthe container
COPY package.json /app/
COPY server.js /app/
# cd to diractory 
WORKDIR /app
#intall npm install in the countainer
RUN npm install 
#intall socket.io for the server
RUN npm install socket.io 
# last cmd in docker file and start app 
CMD ["node","server.js"]
