# Use official Node.js 18 image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files first for better caching
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy all application files
COPY . .

# Expose the application port
EXPOSE 4001

# Start the application
CMD ["npm", "start"]
