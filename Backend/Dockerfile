# Use lightweight Node.js 18 image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install dependencies first for better caching
COPY package*.json ./
RUN npm install --production

# Copy application files
COPY . .

# Set environment variables
ENV PORT=4001
ENV NODE_ENV=production
ENV MONGO_URL=mongodb://mongo:27017/etshostore

# Expose port
EXPOSE 4001

# Start application
CMD ["npm", "start"]
