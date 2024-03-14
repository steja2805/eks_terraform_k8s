# Use the official Node.js 14 image with Alpine Linux as base
FROM node:14-alpine as base

# Set the working directory within the container to /app
WORKDIR /app

# Create a directory named 'quizzapp' within the /app directory
RUN mkdir quizzapp

# Change the working directory to /app/quizzapp
WORKDIR /app/quizzapp

# Copy package.json and package-lock.json (if exists) from the current directory into the container
COPY package*.json ./

# Install dependencies defined in package.json
RUN npm install

# Copy the entire current directory (containing the application source code) into the container at /app/quizzapp
COPY . .

# Build the application using npm run build
RUN npm run build

# Start a new stage of the Dockerfile
FROM node:14-alpine

# Copy the built application from the previous stage (base) into this new stage
COPY --from=base /app/quizzapp ./

# Expose port 3001 to allow external connections to the application
EXPOSE 3001

# Define the default command to run the application when the container starts
ENTRYPOINT ["npm","start"]
