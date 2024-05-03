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

# Command to start the frontend server
CMD ["npm", "start"]