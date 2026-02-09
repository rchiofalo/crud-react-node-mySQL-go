# use node 18 alpine as base image
FROM node:18-alpine

# set working directory
WORKDIR /app

# copy package files and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# copy application code
COPY index.js ./

# expose the backend port
EXPOSE 8800

# start the server
CMD ["node", "index.js"]
