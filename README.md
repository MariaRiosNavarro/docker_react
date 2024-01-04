# React + Docker

VERSION A: [How to Use Docker with React and Vite](https://www.webdevolution.com/blog/how-to-use-docker-with-react-and-vite)

Create Dockerfile

```
# Use an official Node.js runtime as a parent image
FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of your application code to the working directory
COPY . .

# Expose a port to communicate with the React app
EXPOSE 5173

# Start your React app
CMD ["npm", "run", "dev"]
```

Create .dockignore

```
README.md
dist
node_modules
package-lock.json
.git
```

IN terminal:

docker build .
docker image ls
docker run --name reactdocker_01 -d -p 8050:5173 c6ab3a2a9231
docker container ls

![code](/img/code.png)
![code](/img/reult.png)

VERSION B: [Running a React Vite App in Docker Using NGINX](https://medium.com/@fullstackmatt/running-a-react-vite-app-in-docker-using-nginx-414ff9a302c5)
