# Lightweight Node image (exam requirement)
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy only package files first
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy rest of the backend code (including static frontend)
COPY . .

# App must run on port 5000 inside container (exam requirement)
EXPOSE 5000

# Start server
CMD ["node", "server.js"]
