# Use a small base image for production
FROM node:13-alpine AS build

# Set working directory
WORKDIR /yolo_client

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the application
COPY . .

EXPOSE 3000

# Command to start the frontend server
ENTRYPOINT ["npm", "start"]