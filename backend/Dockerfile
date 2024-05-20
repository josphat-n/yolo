# Use a small base image for production
FROM node:14-alpine AS build

# Set working directory
WORKDIR /yolo_backend

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the application
COPY . .

EXPOSE 5000

# Command to start the frontend server
CMD ["npm", "start"]