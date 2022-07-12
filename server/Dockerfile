# FROM node:16

# # Create app directory
# WORKDIR /usr/src/app

# # Install app dependencies
# # A wildcard is used to ensure both package.json AND package-lock.json are copied
# # where available (npm@5+)
# COPY package*.json ./

# RUN npm install
# # If you are building your code for production
# # RUN npm ci --only=production

# # Bundle app source
# COPY . .

# EXPOSE 5000
# We don't want to start from scratch.
# That is why we tell node here to use the openjdk image with java 12 as base.
FROM node:16
WORKDIR /usr/src/app
# Create an application director

# The /app directory should act as the main application directory
# Copy or project directory (locally) in the current directory of our docker image (/app)
COPY package*.json ./

RUN npm install

# Expose $PORT on container.
# We use a varibale here as the port is something that can differ on the environment.
EXPOSE 5000

# Start the app
CMD [ "node", "index.js" ]