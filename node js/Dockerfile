# Use the official Node.js 16 base image
FROM node:16-slim

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files (if available)
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the application code to the container
COPY . .

# Expose the application port
EXPOSE 3000

# Define the command to run your app
CMD ["npm", "start"]


