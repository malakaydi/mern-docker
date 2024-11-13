# Use the Node.js LTS Alpine image
FROM node:lts-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the server files
COPY . .

# Expose the port the server will run on
EXPOSE 9000

# Command to start the server
CMD ["npm", "start"]
