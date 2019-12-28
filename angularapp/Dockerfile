# stage 1 : used for build the image which generate the dist folder which contains all 
# deployable file for angular project

#getting node image using latest version of it
FROM node:latest as node  
# setting working directory to /app 
WORKDIR /app
#copy current folder content(all content in which Dockerfile is present) inside the docker
# container /app folder
COPY . .
#run npm install in the container
RUN npm install
#generate dist folder which contains all deployable files
RUN npm run build --prod

# stage 2 we are using another image inorder to run the application

#pull nginx image
FROM nginx:alpine

# copy files from stage 1 to the default folder of nginx which is used for hosting angular app 
COPY --from=node /app/dist/angularapp /usr/share/nginx/html

# dist/angularapp outputPath": "dist/angularapp" in angular.json file

