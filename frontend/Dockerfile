# use node 18 alpine as base image
FROM node:18-alpine

# set working directory
WORKDIR /app

# copy package files and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# copy all source files
COPY . .

# expose the vite dev server port
EXPOSE 5173

# start vite dev server, bind to 0.0.0.0 so it's accessible outside the container
CMD ["npx", "vite", "--host", "0.0.0.0"]
