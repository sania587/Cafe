# Use official Node.js 18 Alpine image as base
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Expose port 3005 (assumed port for payment-services)
EXPOSE 3005

# Start the service
CMD ["node", "index.js"]
