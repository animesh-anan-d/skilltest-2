# Use Node base image
FROM node:18-alpine

# Set working dir
WORKDIR /app

# Copy files
COPY . .

# Install dependencies
RUN npm install

# Expose port
EXPOSE 3000

# Start app
CMD ["node", "app.js"]
