FROM node:20

WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the app
RUN npm run build

# Install a simple HTTP server for serving static content
RUN npm install -g http-server

# Expose the port the app runs on
EXPOSE 3000

# Start the app
CMD ["http-server", "dist", "-p", "3000"]
