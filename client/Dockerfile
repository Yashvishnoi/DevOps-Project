FROM node:alpine

WORKDIR /usr/app

COPY package*.json ./
RUN npm install
COPY . .
# EXPOSE 3000:3000
# EXPOSE 5000:5000
CMD ["npm","start"]
