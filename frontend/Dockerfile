# Fetching the latest node image on alpine linux
FROM node:alpine AS builder

# Declaring env
ENV NODE_ENV development

# Setting up the work directory
WORKDIR /react-app

# Installing dependencies
COPY ["package.json", "package-lock.json*", "./"]
RUN npm run build

# Copying all the files in our project
COPY . .

EXPOSE 3000

# Starting our application
CMD npm start