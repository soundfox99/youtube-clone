# Use an official Node runtime as a parent image
FROM node:18

# set the working directory in the container to /app
WORKDIR /app

# Copy pacage.json and package-lock.josn into hte working directory
COPY package*.json ./

# Install ffmpeg in the container
RUN apt-get update && apt-get install -y ffmpeg

# Install any needed packages specified in package.json
RUN npm install

# Copy app source inside the docker iamge
COPY . .

# Make port 3000 available outside this container
EXPOSE 3000

# Define the command to run your app using CMD (only one CMD allowed)
CMD [ "npm", "start" ]