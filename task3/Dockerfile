# Use the official Node.js 16 image based on Alpine Linux
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /home/ilovedocker/app

# Copy the package.json and package-lock.json from the subdirectory packages to the working directory
COPY packages/package*.json ./

# Install the dependencies
RUN npm install

# Copy the source code from the subdirectory src to the working directory
COPY src/ ./

# Expose port 3032
EXPOSE 3032

# Command to run the application
CMD ["node", "main.js"]
