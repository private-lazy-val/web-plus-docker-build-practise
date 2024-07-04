# Use the official Node.js 16-alpine image as the base image
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /home/ilovedocker/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Copy hello.sh to the working directory
COPY hello.sh .

# Make hello.sh executable
RUN chmod +x hello.sh

# Set the default command to run the hello.sh script
ENTRYPOINT ["sh", "hello.sh"]
