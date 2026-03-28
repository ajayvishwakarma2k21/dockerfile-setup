# Use Node 18 on Alpine Linux
FROM node:18-alpine

# Set working directory inside the container
WORKDIR /app

# Copy only package files first (layer caching)
COPY package.json package-lock.json ./

# Install dependencies using npm ci
RUN npm ci

# Copy the rest of the application code
COPY . .

# Expose port 5000 (the port your backend runs on)
EXPOSE 5000

# Start the server
CMD ["node", "server.js"]