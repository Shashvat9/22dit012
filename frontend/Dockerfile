# Base image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy project files
COPY . .

# Build the project
RUN npm run build

# Expose the server port
EXPOSE 3000

# Serve the application
CMD ["npx", "serve", "-s", "build"]
