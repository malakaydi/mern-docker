# Use the Node.js LTS Alpine image
FROM node:lts-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the client files
COPY . .

# Build the React application
RUN npm run build

# Install a lightweight HTTP server to serve the static files
RUN npm install -g serve

# Expose the port that the client will run on
EXPOSE 3000

# Command to serve the built React application
CMD ["serve", "-s", "build"]
